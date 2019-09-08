## FHIR Repository Options

### HL7 FHIR Servers for testing

This page [lists FHIR servers](https://wiki.hl7.org/index.php?title=Publicly_Available_FHIR_Servers_for_testing) that are publicly available for testing. These are public services provided by volunteers and HL7 makes no representations concerning their safety or reliability. 

In order to avoid spam etc, the servers are generally password protected. A contact is provided to get a password.

|FHIR Server | Bunsen | MS FHIR Opensource/<br>Managed | Google FHIR | Vonk FHIR (licensed) | HAPI FHIR | Smile CDR |
|------------|--------|----------------------------|-------------|----------------------|-----------|-----------|
|RESTful APIs|No    |Weak |Yes |Yes |Yes |Yes |Yes|
|Authentication|N/A|No/Yes|Yes|Yes|No|Yes|
|Bulk Insert Endpoints/<br>Tools|Yes|No|Yes|Yes|Yes|Yes|
|FHIR Version|R4<br>(python)|STU3|STU3|R4|R4|R4|
|Database control/<br>location|Yes/On premise|No/Cloud|No/<br>Cloud|Yes/On premise|Yes/On premise|Yes/On premise|
|Data security/<br>Compliance|N/A|Yes/<br>Unknown|Yes|N/A|N/A|N/A|
|External Terminology Server|No|No|No|Unknown|No|No|
<td colspan = "7" align="right"> Sai Simhadri, Raju Hemadri, Vandana Chopra</td>


## Scope and Purpose
* Our scope is limited to setting these servers using the documentation available without any expert consultation
* We have set them up on develop's local machine to conduct a high-level review and have hands-on experience to evaluate their fit int CDMH Phase II architecture
* They were compared with each other based on their ability to do RESTful APIs, Authentication, Bulk Support, FHIR Version supported, Access to backend database and data security/compliance

## Bunsen
**Pros**
* Provides FHIR analytic capabilities via a Java and Python API using FHIREncoders
* Bunsen also allows users to load data via JSON or XML using spark map functions or directly load fhir bundles
* Provides functionality to load FHIR Bundles to Spark and save all entities within a bundle to a distinct table (e.g. observation, condition and so on)
* Users can use Spark SQL or underlying Java/Python APIs to perform queries on loaded data (supports complex queries)
* Converts results of a Bunsen query back into bundles
* Supports R4 Python APIs

**Cons**
* Does not provide/expose RESTful APIs
* An intermediate component is required to convert FHIR to Spark SQL
* Cannot control the query since it is not a web API call (might be hard to direct it to Adeptia agent)
* Users must load terminologies into a different Spark database. Cannot configure to an external terminology service

## MS FHIR Server
**Pros**
* Deployment is easy
* Creates search indices which are helpful while querying
* Advantages of Cosmos DB
* References to other resource types
* Recovery of deleted resources

**Cons**
* Azure API for FHIR is still in preview phase (does not confirm to API standards)
* The id of the resource is replaced with a GUID and stored in Cosmos DB (Original patient id is not preserved)
* Because of this masking of Id, it is not possible to query with patient Id. Users can only search for patients by their Cosmos GUID instead of the actual patient ids
* Duplicate records or records with same patient id are treated as distinct records in Cosmos DB
* Searching with invalid filters/values returns all the resources of that type instead of returning an empty result or error
* No endpoint to post multiple records at a time. So we cannot do an incremental update to the FHIR server from our data model (for e.g. inserting data from OMOP to MS FHIR)
* No proper API endpoint to insert data (accepts objects on “https://aspefhirservice.azurewebsites.net/Patient” or “https://aspefhirservice.azurewebsites.net/Patient?activity=false”), security risk of anyone being able to insert data
* No default authentication enabled for open source deployment
* No support for R4 FHIR version yet (slated for 2019)
* FHIR server will not be on Data Provider physical location, it will be on cloud
* Managed service deployment failed thrice in azure environment

## Google FHIR Server
**Pros**
* Supports getting all patient compartment resources
* Have a powerful API and maintains API standards
* Bulk import and export from/to Cloud Storage to FHIR data store
* Supports batch and transactions inserts
* Supports all FHIR STU3 resources
* Support for DICOM and de-identification 
* Publicly available NIH Chest X-Ray dataset and Cancer Imaging Archive datasets
* Setup notifications when there is change to your datastore 
* Supports strong referential integrity
* Security using oauth2.0 for REST endpoints

**Cons**
* Google FHIR API is in beta (pre-release) state and might change 
* FHIR server will not be on Data Provider physical location, it will be on cloud 
* No support for FHIR R4 version yet
* No recovery of deleted resources
* No control over the data store as it is a managed service
* Id is masked into GUID when storing in to the data store
* Limitations on search

## Vonk FHIR Server
**Pros**
* Supports getting all patient compartment resources
* Supports RESTful API
* Supports authentication in licensed version
* Supports all FHIR STU3 resources (supports custom resources too)
* Can be configured with various databases like MongoDB, SQL Server, SQLite, Azure Cosmos DB
* VonkLoader to do bulk upload resources to FHIR server 
* Can be installed and hosted on Data Partner environment 
* Control over the data base
* Validation on incoming resources (Off, Core, Full)
* Exposes client libraries with various functionalities
* Separate portal to manage your content (upload .json or .xml, bundle, .zip or batch)
* Supports Permissive or Strict parsing

**Cons**
* Limited support for terminology operations
* Masks user given id and replaces with a GUID
* Trial version does not expose all the functionalities/capabilities
* Limitations on search
* No support for bulk operations
* Security
* Support for future releases

## HAPI FHIR Server 4.0.0
Released on August 14, 2019
"http://hapifhir.io/" </br>
* A new consent framework called _ConsentInterceptor_ that can be used to apply local consent directives and policies, and potentially filter or mask data has been added
* Initial support for draft FHIR R5 resources has been added
* Support for _GraphQL_ and the _filter search parameter has been added
* The ability to perform cascading deletes has been added

## HAPI FHIR 3.8.0 (Hippo) release: (May 2019)
* New Interceptor Framework
    * massive architectural change with very little user-visible differences at first
    * Interceptors will be able to be attached to any event in HAPI FHIR
    * Interceptors can be global or thread specific
* Interceptors: Progress
    * create new framework (100% complete)
    * maintain backwords compatibility
    * convert existing interceptors to use new framework (50% complete)
    * introduce pointcuts to internal elements of JPA server (50% complete)
    * introduce performance utilities for JPA server (25%)
    * introduce consent service using framework (25%)
* JPA Starter Project
    * properties file now configures everything:
    * database platform		
    * FHIR features
    * Subscriptions (REST Hook, Email, Websocket)
    * CORS
    * [jpaserver starter](https://github.com/hapifhir/hapi-fhir-jpaserver-starter)
* Security Fix in Testpage Overlay <br>
  a potential scripting vulnerability in the Testpage overlay was discovered
		this vulnerability could allow unintended disclosure of cookies, etc
		users of the testpage overlay are recommended to upgrade immediately
* Server Enhancements <br>
 JSON Patch has been rewritten to be more complete, more robust, and have better error message
* Validator Enhancements
    * support for Questionnaire enableWhen 
    * many ValueSet-based code validations can now be performed without needding Lucene
    * many fixes involving complex slicing validation
* JPA Enhancements
    * many performance enhancements
    * composite search parameters are now used in more cases for better performing searches
    * a number of corner-case search bugs have been fixed
    * $expunge operation is now much more performance
    * Client ID mode introduced: it is now possible to use numeric client assigned IDs (not default, but can be turn on)
    * migrator tool now supports migration from 2.5
* What's Next?
    * ongoing work on interceptor APIs and consent
    * work is beginning on an EMPI API
    * Bulk data support - Import/Export
    * Terminology service performance enhancements (ValueSet expansion/validation enhancements)

#### Back to [home](https://data2health.github.io/data-harmonization/)

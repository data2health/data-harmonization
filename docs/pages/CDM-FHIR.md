## Common Data Model (CDM) - FHIR Gap Analysis

### Harmonization of various Common Data Models and Open Standards for Evidence Generation

#### Project Summary
The goal of this project is to facilitate the use of Read World Data (RWD) sources (e.g., claims, Electronic Health Records (EHRs), registries, electronic Patient Reported Outcomes (ePRO) to support evidence generation for regulatory and clinical decision making. 

Examples of the CDMs, reflecting diverse data sources millions of lives, to be used in this project include:
* National Patient-Centered Clinical Research Network (PCORnet)
* Sentinel
* Observational Health Data Sciences and Informatics (OHDSI)
* Informatics for Integrating Biology and the Bedside (i2b2)

For this project, we also aim to collaborate with the following Standards Development Organizations (SDOs) and consortia:
* Clinical Data Interchange Standards Consortium (CDISC)
* Health Level Seven (HL7)
* Healthcare Services Platform Consortium

#### Project Background
In order to achieve a sustainable data network infrastructure, promote interoperability and foster the creation of a LHS as laid out in the Connecting Health and Care for the Nation a Shared Nationwide Interoperability Roadmap, there is a need to map and transform data across various Common Data Models (CDMs) and leverage open-source standards. By mapping various CDM data elements and leveaging existing OS PCORTF investments, it is feasible to reuse the data, methods and other resources from each network (e.g. PCORNET, Sentinel, OHDSI, i2b2) thereby providing PCOR researchers with access to larger and more diverse types of RWD (with appropriate data partner permissions).

### Why So Many CDMs
* Most created with clinical data standard were insufficient (HL7 V2, V3)
* Many research efforts
    * Virtual EMR
    * OMOP → OHDSI
    * HMOrn → POPMedNet → Sentinel → PCORNet
    * I2b2 Shrine

### Have Clinical Standards Caught Up FHIR Phenomenon
* FHIR has emerged over the past five years
* Now endorsed and supported by:
    * Government (ONC, NIH, CDC, FDA, VA, CMS, DOD)
    * Industry (Argonaut group)
    * Payers (da Vinci group)
    * Academia (informatics groups)
    * Community Providers
    * HIEs

### Is FHIR Ready to become Canonical Hub CDM?
* Con:
    * FHIR not fully specified/completed (still drafts)
    * It is a messaging specification, not a model
    * Deliberately underspecified (bindings optional)
* Pro:
    * Bindings can be national (US Core, ACT)
    * Very large development community (Admin to OMICS)
    * Native support by EHRs, minimal ETL
    * FHIR “Resources” as de facto logical model
    * Physical model irrelevant behind conformant server

### Does Anybody Embrace This?
* Major IT organizations offer FHIR servers
* FHIR “objects” being considered by HL7
    * Persistent objects in HBase NOSQL systems
* More sophisticated FHIR query specifications
    * FHIR Bulk
    * FHIR Bundle
    * FHIR SQL
    * CQL to FHIR

### Resources relevant to addressing the CDM FHIR gap:
* [Common Data Models (PCORnet CDM, i2b2, OMOP and Sentinel) to FHIR (FDA/NCATS/CDC/NCI)](https://github.com/data2health/data-harmonization/wiki/CDM-FHIR-Transformation)
* [OMOP to FHIR (Mayo)](https://github.com/BD2KOnFHIR/FHIROntopOHDSI)
* [Camp FHIR / i2b2 ACT (UNC)](https://github.com/NCTraCSIDSci/camp-fhir)

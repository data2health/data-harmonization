[Github.io](https://data2health.github.io/data-harmonization/)

# data-harmonization
Clinical data in CTSA hubs are not readily queryable in a federated fashion.  Many efforts exist to address this, including TriNetX, ACT, PCORNet, and OHDSI among others.  Unifying these with an HL7 FHIR framework is an aspiration. 

Enabling the CTSA to function as a federated network of clinical data, supporting multicenter research is among the core goals of the program. This project advances that agenda through common data model harmonization.

## Problem statement
Data respositories across CTSA hubs need to have semantic and syntactic alignment to support federated query.  This must impose a minimal maintenence burden on CTSA hub sites.  Leveraging the native FHIR APIs, no proposed as required for US EHRs by CMS, would mitigate ETL costs and maintenence issues.

## Project description
Harmonize the data ecosystem. An improved data ecosystem will enhance and extend existing work being performed on the NCATS Data Translator system, which integrates clinical and translational data at scale for mechanistic discovery, as well as other emergent systems such as the NIH Commons. We will apply our strengths and existing activities to make data FAIR-TLC: Findable, Accessible, Interoperable, and Reusable, as well as Traceable, Licensable, and Connected. We will assist contributors and users to develop and apply data standards, Common Data Elements (CDEs), and other commonly utilized data models such as FHIR and OHDSI. We will extend and supplement infrastructure, training, and collaborative environments to enable data to be shared openly, so that groups can collaborate on its harmonization based on specific needs or standards. The data ecosystem will provision CTSA-wide quality assurance reports and data quality assessment, as well as gold-standard datasets and synthetic clinical data sets. Fundamentally, we aim to develop an open-science ethos and unite CTSA community data sharing with broader global efforts.

## Alignment to program objectives
TODO see [here](https://github.com/data2health/roadmap/blob/master/cd2h-foa.md)

### Sub-projects
- [Clinical adaptor](https://github.com/data2health/clinical-adaptor)

### Related Projects
- [HOT FHIR](https://github.com/data2health/hot-fhir-projects)
- [ehr2HPO](https://github.com/data2health/ehr2HPO.prj)

## Contact person

Point person (github handle) | Site | Program Director
----------|--------------|---------------
Tricia Francis (@tricfran) | JHU | Chris Chute (@cgchute)

## Leads 

Project scientific leadership: 

Lead(s) (github handle) | Site
----------|--------------|
Chris Chute (@cgchute) | JHU 


## Team members 

Team members are listed [here](https://github.com/data2health/data-harmonization/blob/master/team.md). 

## Repositories

Many repositories could be listed here, including FHIR sites and CDM data models.  However, for parsimony, we presently list the main FHIR project and the NCATS supported clinicalprofiles.org.

- https://www.hl7.org/fhir
- http://model.clinicalprofile.org
- https://github.com/NCTraCSIDSci/camp-fhir

## Deliverables
Key long-term deliverables
- A coherent common data model across CTSA hubs, arising naturally from their EHR sources.
- Shared terminology services across the CTSA community 

## Milestones 
Milestones are listed, though at present are quite general.

## Evaluation
Evaluation of data harmonization will ultimately rest with its impact on our community.  The goal is to enable federated query and inferencing at scale across the CTSA community.  There are likley to be many lesser advantages and consequences.  Several evaluation issues are in place, though we expect they will evolve with time.  

## Education
We anticipate substantial need to educated the CTSA community about elements of the well-known FHIR specification relevent to translational research.  In particular, the notion of managing FHIR as a canonical model, with migration paths to traditional common data models (e.g. OMOP/OHDSI, PCORNet, ACT, etc.)

## Explore Our Work
* [Federated Data Query Workshop May 20 & 21st, 2019: Subject Matter Expert Slide & Video Presentations](https://drive.google.com/drive/folders/1kgcoV8BW_9Zg7XLwObw9HXAO4aJLamQQ?usp=sharing) 
* [Clinical Data Harmonization and Federated Query for Translational Research: Reflections and Report on a CD2H Workshop](https://docs.google.com/document/d/1fda3KLqPfDsAJ3Ah1MdqpxC4PSoCXBNy9ATWSiFG8CY/edit?usp=sharing) 
    * This report, developed by a small team of representatives across the CTSA community, is ready for input across the wider CTSA community.  Your review and input is requested in this collaborative document.   
* [CDM-FHIR Mappings](https://drive.google.com/drive/folders/1Mrt0xFfvcYhOfoAq_KnT7R5bYk7TZ6h0?usp=sharing)
    * The CDM-FHIR Gap Analaysis Task Team has complied the most comprehensive mappings assembled to date. If you know of any other mappings that you do not see here, please add.    
* [Data Harmonization Maturity Model](https://docs.google.com/document/d/1IKKbSxe19ZgayDnv5cqTUzDswNGWQvKZNUc2IgZvaL8/edit?usp=sharing)
    * The Sustainability and Change Managenet Task Team has developed a data harmonization maturity model and it is ready for wider CTSA Community input.  Are there other factors that should be considered?


## Get involved
We encourage the community to get involved. 

We are looking for community participation in the following areas:
- [CDM-FHIR Gap Analysis](https://drive.google.com/drive/folders/1TUwrDaH-2eRv3ofkY1tm2NbX7XttK3hx?usp=sharing)
- [Sustainability and Change Management](https://drive.google.com/drive/folders/16vL1yckE9rliOoVB6yufTN7x_yOOAxUH?usp=sharing) 
- [FHIR Server Options](https://docs.google.com/document/d/1_32CiANmo8W1TRG5IofqzJZmpgtu-s1jNenXu_efmtg/edit?usp=sharing)
- [HL7 Engagement](https://docs.google.com/document/d/1Li6X6W2ck_XhYWr6RhpHtAaFI8rJmJAnjVQwvokhy14/edit?usp=sharing) 

If you are interested in participating, please [onboard here](http://bit.ly/cd2h-onboarding-form) or contact Tricia Francis at pfranci4@jhu.edu with any questions.

## Working documents
Documentation for the various data harmonization task teams can be found at [this Google drive folder](https://drive.google.com/drive/folders/14cMMsDExi7KsmkX49d8_zX7ojeCuW7_P?usp=sharing)
and project specific work may be in this GitHub using the wiki or .md files.


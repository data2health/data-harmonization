# data-harmonization
Clinical data in CTSA hubs are not readily queryable in a federated fashion.  Many efforts exist to address this, including TriNetX, ACT, PCORNet, and OHDSI among others.  Unifying these with an HL7 FHIR framework is an aspiration. 

Enabling the CTSA to function as a federated network of clinical data, supporting multicenter research is among the core goals of the program. This project advances that agenda through common data model harmonization.

## Problem statement
Data respositories across CTSA hubs need to have semantic and syntactic alignment to support federated query.  This must impose a minimal maintenence burden on CTSA hub sites.  Leveraging the native FHIR APIs, no proposed as required for US EHRs by CMS, would mitigate ETL costs and maintenence issues.

## Project description
(we will migrate these from the Project Matrix for you)

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum pretium a felis non scelerisque. Etiam molestie nisi ut mi viverra dictum. Nunc et tempor quam. Maecenas a viverra sapien. Aliquam lacinia sagittis lorem ac sodales. Fusce justo mi, cursus sed metus sed, ornare vestibulum mauris. Donec in orci ornare, facilisis nisl ut, congue libero.

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

Project scientific leadership, should be 1-3 persons. 

Lead(s) (github handle) | Site
----------|--------------|
Chris Chute (@cgchute) | JHU 


## Team members 

No action required here, a list of team members will be imported and linked below.

See https://github.com/data2health/project-repo-template/tree/master/team.md

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


## Get involved
We encourage the community to get involved. 

We are looking for community participation in the following areas:
- [HL7 Engagement](https://docs.google.com/document/d/1Li6X6W2ck_XhYWr6RhpHtAaFI8rJmJAnjVQwvokhy14/edit?usp=sharing)
- [CDM-FHIR Gap Analysis](https://drive.google.com/drive/folders/1TUwrDaH-2eRv3ofkY1tm2NbX7XttK3hx?usp=sharing)
- [FHIR Server Options](https://docs.google.com/document/d/1_32CiANmo8W1TRG5IofqzJZmpgtu-s1jNenXu_efmtg/edit?usp=sharing)
- [Sustainability and Change Management](https://drive.google.com/drive/folders/16vL1yckE9rliOoVB6yufTN7x_yOOAxUH?usp=sharing) 

If you are interested in participating, please [onboard here](http://bit.ly/cd2h-onboarding-form)


## Working documents
Documentation for the various data harmonization task teams can be found at [this Google drive folder](https://drive.google.com/drive/folders/14cMMsDExi7KsmkX49d8_zX7ojeCuW7_P?usp=sharing)
and project specific work may be in this GitHub using the wiki or .md files.


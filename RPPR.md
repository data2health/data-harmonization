# Budget
Don't edit this - the RPPR generator populates this section

# Research Design
Working with the CTSA and HIT standards communities to identify a canonical data model for CTSA elements, and evolving in partnership with traditional research common data models migration pathways.  FHIR is proposed as the most practical basis for such a canonical model.
# Methodology
We anticipate many points of engagement:
*	Primary consultation with CTSA hubs through workshops, video conference, and collaboration tools
*	Leverage linkages to standards developers such as HL7 and ONC, focusing on FHIR resources
*	Engage traditional common data models to develop or validation inter-model transformation
# Expected Outcomes
The primary outcomes for this project are:
* a common data model for CTSA leveraging clinical standards such FHIR
* migration pathways to and from the FHIR server and traditional data models
* the beginning of federated query that can scale across the CTSAs with minimal impedance 

# Deliverables
Key long-term deliverables
- A coherent common data model across CTSA hubs, arising naturally from their EHR sources.
- Shared terminology services across the CTSA community 

# Timeline (monthly)
* 6/1 – Experiment with FHIR server as back-end for CTSA EHR data
* 6/1 – Begin evaluation of legacy data models into FHIR servers
* 7/1 – Incorporate one innovative FHIR resource, relevant to translational research, into FHIR server as demonstration
* 8/1 – Explore data transfer into FHIR server via FHIR Bulk API
* 9/14 – Participate in HL7 FHIR Hackathon in Atlanta
* 9/26 – Demonstrate FHIR server functionality at CTSA Program Meeting
* 1/1 – Deploy FHIR server at two CTSA hubs
* 1/1 – Demonstrate migration from legacy data model into FHIR server
* 1/1 -  Begin exploring federated query via FHIR Bulk API
# Potential Pitfalls and Alternative Strategies
A significant number of FHIR servers, open source and vendor supported, are appearing.  Ideally CTSA hubs would agree on a single FHIR serverThese   Further, while supported servers are stable, they come with maintenance costs that some CTSA hubs may prefer not to support.
* An alternative is to ensure that whatever FHIR server choices are made, suitable open-source alternatives are readily available

Data transformation is expected to be minimal from EHRs to FHIR servers via FHIR APIs.  However, the output of FHIR APIs is not uniformly conformant to specification.  Furthermore, FHIR is deliberately underspecified.  
* Working with traditional common data models, and especially the ACT effort already within CTSA, derive a fully specified extension of the clinical FHIR specification suitable for translational research
* Begin to design, build, validate, and incrementally enhance data transformation services that ensure comparable and consistent data in CTSA FHIR servers


# Y3 (July 1, 2019-June 30, 2020) Accomplishments 
The following content is from the June 30 - Dec 30, 2019 mid year progress report [here](https://docs.google.com/document/d/1Y-dYvG5aePtBhje18SnPFjXzLVW7rC_qtjDv_RgEs68/edit#bookmark=id.fk4h20ocdh0w).  Please add progress for Jan 1 - June 30th, 2020. 

* A common data model for CTSA leveraging clinical standards such FHIR:
    * CD2H team is a core collaborator with CDMH & CCDH  projects developing ‘NIH-wide stack’ architecture which addresses FDA, NCI, CDC and CTSA use cases for a common clinical data model and includes leveraging available FHIR (present & future) resources in addition to NCI (caDSR / LexEVS) components. Scope of this collective effort is inclusive of, but broader than previously stated CTSA focused use cases.In this funding period, we have made substantial progress in co-leading this pan-agency endeavor.
    
* Migration pathways to and from the FHIR server and traditional data models:
    * Activities: 1) Examination of gaps between CTSA implementation  instances of PCORNet and existing FHIR resources at UNC (CAMP-FHIR) lead by Data Harmonization Core community lead Emily Pfaff 2) Analysis of proposed migration pathways utilizing CAMP-FHIR architecture / implementation in a mock implementation review yielding a) gaps in process and content  b) a repeatable process blueprint to be applied to additional data model implementations (eg: OMOP, i2b2 ACTs) and c) task list to be applied to a projection / action plan in order to develop CAMP-FHIR implementation specific alignment to FHIR Server and NIH-wide stack harmonization architecture

* The beginning of federated query that can scale across the CTSAs with minimal impedance:
    * As above: repeatable analysis process has been established aimed at eliciting gaps between present capabilities in implementation instances of common data models (OMOP, I2b2 ACTs, Sentinel…) which will inform nascent NIH-wide data sharing architecture as well as surface gaps from data-model specific implementations, thus producing task lists which address implementations at specific CTSAs.  Completion of these processes - first the analysis, then developing implementation guidance has the goal of realizing increased data-sharing capabilities at individual CTSA sites.

* A coherent common data model across CTSA hubs, arising naturally from their EHR sources:
    * Progress toward a common data model.  CDM-FHIR Gap Analysis Task Team Meeting outcomes as of end of year here and special face-to-face meeting here. A number of conversations across multiple organizations (FDA, CDC, CD2H, CCDH, CDMH) are occuring. 

* Shared terminology services across the CTSA community:
    * See HOT Ecosystem progress report. 

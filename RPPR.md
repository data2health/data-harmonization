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

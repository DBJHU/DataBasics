# DataBasics:  A Resource on Research Using Electronic Health Records

# Introduction

Electronic Health Records (EHR) have revolutionized the way healthcare information is stored, accessed, and used across the medical industry. This primer aims to provide a lay audience with an understanding of EHR data, its history, key definitions, and insights into the standards and methodologies for extracting EHR data for research. We'll explore HL7, CDA, and FHIR standards, the differences between direct EHR data extraction and using OAuth 2.0, and review common data models along with the pros and cons of various data extraction processes.

## History of EHR Data

EHR data's history dates back to the 1960s with the earliest systems focusing on simple data capture and storage. Over the decades, EHR systems have evolved significantly, incorporating more complex data types such as imaging and laboratory results, and enabling more sophisticated data sharing and interoperability. The goal has always been to improve patient care, streamline healthcare operations, and facilitate health research.

## Definitions

- **EHR (Electronic Health Record):** A digital version of a patient's paper chart. EHRs contain the patient's medical history, diagnoses, medications, treatment plans, immunization dates, allergies, radiology images, and laboratory test results. EHRs are designed to be shared with other providers across more than one healthcare organization to provide accurate, up-to-date, and complete information about patients at the point of care.
  
- **HL7 (Health Level Seven International):** A set of international standards for the exchange, integration, sharing, and retrieval of electronic health information. HL7 standards support clinical practice and the management, delivery, and evaluation of health services.

- **CDA (Clinical Document Architecture):** An HL7 standard designed to allow healthcare providers to exchange clinical documents, such as discharge summaries and progress notes, in a readable and structured format.

- **FHIR (Fast Healthcare Interoperability Resources):** The latest standard by HL7, designed to enable healthcare information to be available, discoverable, and understandable globally, and to support a wide range of applications, including mobile apps, cloud communications, and data analysis algorithms. For a comprehensive understanding of Fast Healthcare Interoperability Resources (FHIR) concepts and data models, refer to the [Microsoft Learn documentation on FHIR](https://learn.microsoft.com/en-us/training/modules/health-data-fast-healthcare-interoperability-resources/concepts-data-model). From this training, "US Core provides the framework for the implementation of regulations that are driven by the Centers for Medicare & Medicaid Services (CMS) and the ONC Final Rule [https://www.healthit.gov/topic/oncs-cures-act-final-rule]. Payors and providers across the United States who accept Medicare/Medicaid patients implement FHIR® by following the profiles that are defined in US Core.

- **OAuth 2.0:** An authorization framework that enables applications to obtain limited access to user accounts on an HTTP service, such as Facebook, GitHub, and digital health records.
 - NIH's All of Us Study uses OAuth 2.0 via [Sync for Science](https://www.healthit.gov/topic/sync-science).

## Extracting EHR Data

Extracting EHR data can be done directly from the EHR system at a healthcare site or via web-based APIs using protocols like OAuth 2.0. Direct extraction involves accessing the EHR database or data warehouse, often requiring custom queries and significant IT support. OAuth 2.0, meanwhile, allows researchers to access data through predefined APIs with the user's consent, facilitating more standardized and scalable data access.

### Pros and Cons of Different Data Extraction Processes

#### Direct Extraction:
- **Pros:** Can access comprehensive EHR data; allows for custom queries.
- **Cons:** Requires significant IT resources; potential privacy and security concerns; may be time-consuming.

#### OAuth 2.0/API-Based Extraction:
- **Pros:** Standardized access method; scalable; less IT-intensive; enhances data security .
- **Cons:** May offer limited access to EHR data; dependent on the availability and functionality of APIs.

| Extraction Method      | Pros                                                               | Cons                                                              |
|------------------------|--------------------------------------------------------------------|-------------------------------------------------------------------|
| OAuth/API-based        | Standardized access; scalable; less IT-intensive; enhances security by limiting access | May offer limited access to data; dependent on API functionality  |
| Direct Extraction      | Access to comprehensive EHR data; allows for custom queries        | Requires significant IT resources; potential privacy concerns     |


### Common Data Models

Common Data Models (CDMs) standardize the format and terminology of healthcare data from various sources, making it easier to aggregate, share, and analyze data across different systems. Examples include the Observational Medical Outcomes Partnership (OMOP) and the Patient-Centered Outcomes Research Network (PCORnet).

### Data Standards, Common Data Elements, and Validated Instruments

**CDISC:** Clinical Data Interchange Standards Consortium. The Clinical Data Interchange Standards Consortium (CDISC) is a global non-profit organization that develops and supports global data standards to improve the quality and efficiency of clinical research. CDISC standards are designed to facilitate the harmonization of clinical data and streamline research processes from protocol through analysis and reporting. This standardization supports the direct use of EHR data for research and regulatory submissions, making it easier to compare and combine data from different studies or sources.

#### Common Data Elements (CDEs)

Common Data Elements (CDEs) are precisely defined questions and answer choices, along with associated metadata, used in clinical research and patient care. They are intended to promote the collection of standardized data across studies and health records. By standardizing the way data is collected, stored, and exchanged, CDEs enable researchers to more easily compare and combine data from different sources, enhancing data quality and research efficiency.

#### Validated Instruments

Validated instruments are tools or questionnaires that have been scientifically proven to accurately and reliably measure a specific concept or construct, such as symptoms, quality of life, or functional status. Validation involves rigorous testing to ensure the instrument consistently produces accurate data that reflects what it is designed to measure across different populationsand settings.

### Integrating CDISC, CDEs, and Validated Instruments in EHR Data for Research

The integration of CDISC standards, CDEs, and validated instruments into EHR systems and research protocols can significantly enhance the quality, efficiency, and comparability of health data. This integration supports streamlined data collection and analysis, regulatory compliance and submission, and enhanced interoperability.

## Resources and "MUST READ"papers:
### EBMonFHIR-based tools and initiatives to support clinical research

- **Authors:** Alper B. S.
- **Journal:** Journal of the American Medical Informatics Association : JAMIA, 30(1), 2022.
- **DOI/URL:** [10.1093/jamia/ocac193](https://doi.org/10.1093/jamia/ocac193)
- **PMC:** [PMC9748541](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9748541/)

### HL7 FHIR-based tools and initiatives to support clinical research: a scoping review

- **Authors:** Duda SN, Kennedy N, Conway D, Cheng AC, Nguyen V, Zayas-Cabán T, Harris PA.
- **Journal:** J Am Med Inform Assoc, 29(9), 2022.
- **DOI:** [10.1093/jamia/ocac105](https://doi.org/10.1093/jamia/ocac105)
- **PMID:** 35818340; **PMCID:** PMC9382376.
- **URL:** [PubMed](https://pubmed.ncbi.nlm.nih.gov/35818340/)

### Technology-Enabled Clinical Trials: Transforming Medical Evidence Generation

- **Authors:** Marquis-Gravel G, Roe MT, Turakhia MP, Boden W, Temple R, Sharma A, Hirshberg B, Slater P, Craft N, Stockbridge N, McDowell B, Waldstreicher J, Bourla A, Bansilal S, Wong JL, Meunier C, Kassahun H, Coran P, Bataille L, Patrick-Lake B, Hirsch B, Reites J, Mehta R, Muse ED, Chandross KJ, Silverstein JC, Silcox C, Overhage JM, Califf RM, Peterson ED.
- **Journal:** Circulation, 140(17), 2019.
- **DOI:** [10.1161/CIRCULATIONAHA.119.040798](https://www.ahajournals.org/doi/10.1161/CIRCULATIONAHA.119.040798)
- **PMID:** 31634011

### For more information on HL7, CDA, and FHIR standards, and on extracting EHR data, you can visit the following websites:

- CDISC: [https://www.cdisc.org/](https://www.cdisc.org/)
- Duke-Margolis International Harmonization of Real World Evidence Standards Dashboard: [https://healthpolicy.duke.edu/projects/international-harmonization-real-world-evidence-standards-dashboard](https://healthpolicy.duke.edu/projects/international-harmonization-real-world-evidence-standards-dashboard)
- HL7: [http://www.hl7.org](http://www.hl7.org)
- FHIR: [http://hl7.org/fhir/](http://hl7.org/fhir/)
- FHIR for Research Workshop (NIH) [https://datascience.nih.gov/fhir-initiatives/researchers-training]
- National Cancer Institute CDE Resource: [https://cde.nci.nih.gov/](https://cde.nci.nih.gov/)
- NIH Common Data Elements: [https://cde.nlm.nih.gov/home](https://cde.nlm.nih.gov/home)
- OAuth 2.0: [https://oauth.net/2/](https://oauth.net/2/)
- OHDSI: [https://www.ohdsi.org/](https://www.ohdsi.org/)
- PCORnet: [https://pcornet.org/](https://pcornet.org/)


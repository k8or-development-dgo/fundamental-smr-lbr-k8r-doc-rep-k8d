# Payload Structure Number `PSN` within the Sambar/LeBar/k8or Web Applications

The document provides a comprehensive overview of Payload Structure Numbers `PSNs` and Payload Resource Numbers `PRNs` within a communication chain in the Sambar/LeBar/k8or web applications. It explains the structure and components of these identifiers, their relationship to each other, and the rationale behind their segment order. PSNs and PRNs play important roles in ensuring data consistency, facilitating seamless interpretation, and enabling efficient data processing and analysis.

## Content

1. **[Payload Structure Number `PSN`](#Payload-Structure-Number-PSN)**
2. **[Payload Resource Number `PRN`](#Payload-Resource-Number-PRN)**
3. **[Relationship Between `PSN` and `PRN`](#Relationship-Between-PSN-and-PRN)**
4. **[Segment Order](#Segment-Order)**
5. **[Rationale for Segment Order](#Rationale-for-Segment-Order)**
6. **[Benefits of the Segment Order](#Benefits-of-the-Segment-Order)**
7. **[Document Metadata](#Document-Metadata)**

<h1 id="Payload-Structure-Number-PSN">Payload Structure Number `PSN`</h1>

A Payload Structure Number `PSN` serves as a blueprint, meticulously defining the structure or schema that data must adhere to within a specific communication chain. It ensures data consistency and facilitates seamless interpretation across various microservices within the chain.

**Structure:** A Payload Structure Number `PSN` is constructed using the following components, concatenated with hyphens:

`c04-ub02130e05-psn05ugd`

- **Communication Chain ID Structure `c04`:**
  - **Prefix:** The Chain ID always starts with the letter `c`.
  - **Number:** A sequential number, starting from 04 and increasing in increments of 4.
  - **Example Chain IDs:**
    - `c04` - Represents the first defined chain in a BLOCK.
    - `c08` - Represents the second defined chain in the same BLOCK.
    - `c12` - Represents the third defined chain in the same BLOCK.
- **Microservice Identifier `ub02130`:** Composed of an alphabetic prefix and a numeric suffix. The alphabetic prefix is constructed by concatenating the initial letter of each word comprising the full microservice name (e.g., `ub` for `user board`. The numeric suffix, a four or five digit number (e.g., `02130`, correlates to the specific Flow and BLOCK within the system where the microservice is originally defined.
  - `ub`: Indicates the event originated in the User Board (ub) microservice.
  - `02130`: A composite number providing contextual details:
    - `021`: Denotes the specific Flow within the ub microservice where the event occurred.
    - `30`: Identifies the BLOCK within the flow where the event happened. BLOCKs group related functionalities within a flow.
- **Execution Order Number `e05`:** Specifies the sequential execution order of a function within its BLOCK.
  - **Prefix:** `e`: Specifies the sequential execution order of a function within its Block
  - **Number:**`05`: This is the first execution of the function within BLOCK. Execution order numbers increment in multiples of 5 `e05`, `e10`, `e15`, etc.)
  - **Example:** 
    - `e05`: for the first execution of the function within particular BLOCK. 
    - `e10`: for the second execution of the function within same BLOCK. 
    - `e15`: for the third execution of the function within same BLOCK.
- **PSN ID `psn05`:**
  - Format: `psn` + number
  - Number: Uniquely identifies the data structure within the microservice function.
  - **For requests, PSN IDs start from 05 and increment by 4 (e.g., psn05, psn09, psn13).**
  - **For responses, PSN IDs start from 14 and increment by 4 (e.g., psn14, psn18, psn22).**
- **Data Type `ugd`:** A categorization of data based on its origin and purpose:
  - `ugd`: User Generated Data
  - `ucd`: User Clicked Data
  - `sgd`: System Generated Data
  - `srd`: System Responded Data
  - `sed`: System Error Data

<h1 id="Payload-Resource-Number-PRN">Payload Resource Number `PRN`</h1>

**Structure:** A Payload Resource Number `PRN` is a unique identifier that references specific data instances within a communication chain. It shares the same structural components as a PSN but with a different purpose. Its elements are:

`c04-ub02130e05-prn05ugd`

- **Communication Chain ID Structure:**
  - **Prefix:** The Chain ID always starts with the letter `c`.
  - **Number:** A sequential number, starting from 04 and increasing in increments of 4.
  - **Example Chain IDs:**
    - `c04` - Represents the first defined chain in a BLOCK.
    - `c08` - Represents the second defined chain in the same BLOCK.
    - `c12` - Represents the third defined chain in the same BLOCK.
- **Microservice Identifier `ub02130`:** Composed of an alphabetic prefix and a numeric suffix. The alphabetic prefix is constructed by concatenating the initial letter of each word comprising the full microservice name (e.g., `ub` for `user board`. The numeric suffix, a four or five digit number (e.g., `02130`, correlates to the specific Flow and BLOCK within the system where the microservice is originally defined.
  - `ub`: Indicates the event originated in the User Board (ub) microservice.
  - `02130`: A composite number providing contextual details:
    - `021`: Denotes the specific Flow within the ub microservice where the event occurred. (See the "Flows and BLOCKs" documentation for details on flows.)
    - `30`: Identifies the BLOCK within the flow where the event happened. BLOCKs group related functionalities within a flow.
- **Execution Order Number `e05`:** Specifies the sequential execution order of a function within its BLOCK.
  - **Prefix:** `e`: Specifies the sequential execution order of a function within its Block
  - **Number:**`05`: This is the first execution of the function within BLOCK. Execution order numbers increment in multiples of 5 `e05`, `e10`, `e15`, etc.)
  - **Example:** 
    - `e05`: for the first execution of the function within particular BLOCK. 
    - `e10`: for the second execution of the function within same BLOCK. 
    - `e15`: for the third execution of the function within same BLOCK.
- **PSN ID `prn05`:**
  - Format: `psn` + number
  - Number: Uniquely identifies the data structure within the microservice function.
  - **For requests, PSN IDs start from 05 and increment by 4 (e.g., prn05, prn09, prn13).**
  - **For responses, PSN IDs start from 14 and increment by 4 (e.g., prn14, prn18, prn22).**
- **Data Type `ugd`:** A categorization of data based on its origin and purpose:
  - `ugd`: User Generated Data
  - `ucd`: User Clicked Data
  - `sgd`: System Generated Data
  - `srd`: System Responded Data
  - `sed`: System Error Data

<h1 id="Relationship-Between-PSN-and-PRN">Relationship Between `PSN` and `PRN`</h1>

- A PSN defines the structure of data, acting as a blueprint for the data format.
- A PRN references specific data instances that adhere to the structure defined by a corresponding PSN.
- Both PSN and PRN share the same communication chain, microservice, and function execution components, ensuring data consistency and traceability within the chain.

<h1 id="Segment-Order">Segment Order</h1>

| Segment   | Position | Rationale                                                    |
| --------- | -------- | ------------------------------------------------------------ |
| `c04`     | 1st      | **Communication Chain ID:** Placing it first establishes the overarching context for the data and facilitates grouping related PSNs and PRNs. |
| `ub02130` | 2nd      | **Microservice ID:** Following the Communication Chain ID, it narrows down the data's origin and processing stage. |
| `e05`     | 3rd      | **Microservice Function Execution Number:** Provides further granularity, allowing tracking of data flow within a microservice. |
| `prn05`   | 4th      | **PSN/PRN ID:** Placed after the context-defining segments, it focuses on the core identifier of the data. |
| `ugd`     | 5th      | **Data Type:** Placing it last provides additional metadata about the data, aiding in filtering and analysis. |

<h1 id="Rationale-for-Segment-Order">Rationale for Segment Order</h1>

The chosen order of segments is designed to optimize data processing, analysis, and traceability within the communication chain.
- **Communication Chain ID:** Identifies the specific sequence of microservices involved in data processing.
- **Microservice ID:** Specifies the particular microservice handling the data.
- **Microservice Function Execution Number:** Indicates the specific function within the microservice that processes the data.
- **PSN/PRN ID:** Uniquely identifies the data structure or instance within the specified context.
- **Data Type:** Categorizes the data based on its origin and purpose.

<h1 id="Benefits-of-the-Segment-Order">Benefits of the Segment Order</h1>

- Efficient Data Retrieval: The order facilitates rapid filtering and retrieval of data based on various criteria.
- Improved Data Analysis: By grouping related data segments, analysis becomes more streamlined and informative.
- Enhanced Traceability: The ordered structure enables easy tracking of data Flow through the communication chain.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Payload Structure Number `PSN` within the Sambar/LeBar/k8or Web Applications |
| | Description | The document provides a comprehensive overview of Payload Structure Numbers `PSNs` and Payload Resource Numbers `PRNs` within a communication chain in the Sambar/LeBar/k8or web applications. It explains the structure and components of these identifiers, their relationship to each other, and the rationale behind their segment order. PSNs and PRNs play important roles in ensuring data consistency, facilitating seamless interpretation, and enabling efficient data processing and analysis. |
| | Identification | TBD | |
| | Version | v0-0-01 | |
| | Format | md | |
| | Revision | This is the first version uploaded to the ChatBOT. |
| | Author | Anna/Barb.Rock |
| | Date | October 11, 2024 |
| Subject Metadata | Alias | TBD |
| |  Name | TBD |
| |  FQID | TBD |
| |  Version | s0-0-01 |
| |  Action | 000010 |
| hGraph Metadata | Alias | none |
| |  Name | none |
| |  FQID | none |
| |  Version | none |
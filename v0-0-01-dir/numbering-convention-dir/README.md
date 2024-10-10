## Sambar/LeBar/k8or Web Application Numbering Convention

This document provides a technical description of the `flows` and their constituent components `BLOCKs` and `legs` within the Sambar/LeBar/k8or web applications.

## Content

1. **[Flows: Sequences of Functionality](#Flows-Sequences-of-Functionality)**
2. **[BLOCKs: Building BLOCKs of Functionality](#BLOCKs-Building-BLOCKs-of-Functionality)**
3. **[Legs: Units of Execution](#Legs-Units-of-Execution)**
4. **[Document Metadata](#Document-Metadata)**

<h1 id="Flows-Sequences-of-Functionality">Flows: Sequences of Functionality</h1>

A flow represents a defined sequence of operations and processes that data and requests follow to achieve a specific functionality or feature within the Sambar/LeBar/k8or web application. 

Each flow is assigned a unique identifier using a `one-` or `three-digit code`. This code signifies the specific function it serves within the Sambar/LeBar/k8or applications.

**Flow List:**

The following sections categorize and list the flows employed within the Sambar/LeBar/k8or applications:

* **Traditional Sambar Flows:** Represent core functionalities within the Sambar web application (e.g., User Registration, User Profile).
* **Integrated Sambar Flows:** Facilitate interaction between Sambar and LeBar functionalities (e.g., Sambar-LeBar User Registration).
* **Traditional LeBar Flows:** Represent core functionalities within the LeBar web application (e.g., User Registration, Purchase LeBar).
* **Integrated LeBar Flows:** Integrate functionalities within the LeBar application (e.g., User Registration, Notification Tab).
* **Traditional k8or Flows:** Represent core functionalities within the k8or web application (e.g., Site Static Page, ChatBOT).

**Flow Identifier Conventions:**

* Flow identifiers consist of a flow identifier prefix followed by the letter `f` and a flow one or three digits number.
* The specific functionality of a flow is not directly encoded in the identifier.

<h1 id="BLOCKs-Building-BLOCKs-of-Functionality">BLOCKs: Building BLOCKs of Functionality</h1>

A BLOCK is a unit within a flow that consists of multiple legs. Each leg is designed to execute a distinct and specific function. These individual legs work together synergistically to achieve the overall purpose of the BLOCK.

**BLOCK Identifier Conventions:**

* BLOCK identifiers consist of a BLOCK identifier prefix followed by the letter `b` and a BLOCK number.
* BLOCK numbering follows a sequential pattern, incrementing by a multiple of 3 (e.g., b3, b6, b9).
* Reserved numbers are strategically inserted between BLOCK numbers to accommodate potential future additions of new functionality within a flow.

**Example BLOCK Identifiers:**

* f2b12: Flow 2, BLOCK 12
* f024b3: Flow 024, BLOCK 3

* **Note:** The first BLOCK in a flow always starts with number 3 `b3`.

<h1 id="Legs-Units-of-Execution">Legs: Units of Execution</h1>

A leg represents a set of resources combined to perform a specific function within a BLOCK. These resources include microservices `MSVs`, event routers `ERs`, and middleware resources.

**Leg Identifier Conventions:**

* Leg identifiers consist of a flow identifier prefix, a BLOCK identifier suffix, and the letter `L` followed by a leg number.
* Leg numbering within a BLOCK follows a sequential pattern, incrementing by a multiple of 4 (e.g., `L4`, `L8`, `L12`).
* Reserved numbers are strategically inserted between leg numbers to accommodate potential future additions of functionality within a BLOCK.

**Example Leg Identifier:**

* F2B3L4: Flow 2, BLOCK 3, Leg 4

* **Note:** The first leg in a BLOCK always starts with number 4 `L4`.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Sambar/LeBar/k8or Web Application Numbering Convention |
| | Description | This document provides a technical description of the `flows` and their constituent components `BLOCKs` and `legs` within the Sambar/LeBar/k8or web applications. |
| | Identification | TBD | |
| | Version | v0-0-01 | |
| | Format | md | |
| | Revision | This is the first version uploaded to the ChatBOT. |
| | Author | Anna/Barb.Rock |
| | Date | October 10, 2024 |
| Subject Metadata | Alias | TBD |
| |  Name | TBD |
| |  FQID | TBD |
| |  Version | s0-0-01 |
| |  Action | 000010 |
| hGraph Metadata | Alias | none |
| |  Name | none |
| |  FQID | none |
| |  Version | none |
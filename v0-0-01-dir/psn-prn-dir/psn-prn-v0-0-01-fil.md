### Payload Structure Number (PSN) Structure Process

A Payload Structure Number (PSN) serves as a blueprint, meticulously defining the structure or schema that data must adhere to within a specific communication chain. It ensures data consistency and facilitates seamless interpretation across various microservices within the chain.

**Structure:** A Payload Structure Number (PSN) is constructed using the following components, concatenated with hyphens:

`c04-ub02130e05-psn05ugd`

- **Communication Chain ID Structure (`c04`):**
  - **Prefix:** The Chain ID always starts with the letter `c`.

  - **Number:** A sequential number, starting from 04 and increasing in increments of 4.

  - **Example Chain IDs:**
    - `c04` - Represents the first defined chain in a BLOCK.

    - `c08` - Represents the second defined chain in the same BLOCK.

    - `c12` - Represents the third defined chain in the same BLOCK.


- **Microservice Identifier (`ub02130`):** Composed of an alphabetic prefix and a numeric suffix. The alphabetic prefix is constructed by concatenating the initial letter of each word comprising the full microservice name (e.g., `ub` for `user board`). The numeric suffix, a four or five digit number (e.g., `02130`), correlates to the specific Flow and BLOCK within the system where the microservice is originally defined.
  - `ub`: Indicates the event originated in the User Board (ub) microservice.

  - `02130`: A composite number providing contextual details:
    - `021`: Denotes the specific Flow within the ub microservice where the event occurred. (See the "Flows and BLOCKs" documentation for details on flows.)
    - `30`: Identifies the BLOCK within the flow where the event happened. BLOCKs group related functionalities within a flow.

- **Execution Order Number (`e05`):** Specifies the sequential execution order of a function within its BLOCK.
  - **Prefix:** `e`: Specifies the sequential execution order of a function within its Block

  - **Number:**`05`: This is the first execution of the function within BLOCK. Execution order numbers increment in multiples of 5 (`e05`, `e10`, `e15`, etc.)

  - **Example:** 
    - `e05`: for the first execution of the function within particular BLOCK. 
    - `e10`: for the second execution of the function within same BLOCK. 
    - `e15`: for the third execution of the function within same BLOCK.

- **PSN ID (`psn05`):**
  - Format: `psn` + number
  - Number: Uniquely identifies the data structure within the microservice function.
  - **For requests, PSN IDs start from 05 and increment by 4 (e.g., psn05, psn09, psn13).**
  - **For responses, PSN IDs start from 14 and increment by 4 (e.g., psn14, psn18, psn22).**
  
- **Data Type (`ugd`):** A categorization of data based on its origin and purpose:
  - `ugd`: User Generated Data
  - `ucd`: User Clicked Data
  - `sgd`: System Generated Data
  - `srd`: System Responded Data
  - `sed`: System Error Data


**Example of the Payload Structure Number (PSN): **

**`c04-ub02130e05-psn05ugd`**

**`c04`**: Communication Chain ID

**`ub02130`**: Microservice ID

**`e05`**: Microservice Function Execution Number

**`psn05ugd`**: PSN ID (structure number 05 for user generated data)

### Payload Resource Number (PRN) Structure Process

**Structure:**

`c04-ub02130e05-prn05ugd`

A Payload Resource Number (PRN) is a unique identifier that references specific data instances within a communication chain. It shares the same structural components as a PSN but with a different purpose. Its elements are:

- **Communication Chain ID Structure:**
  - **Prefix:** The Chain ID always starts with the letter `c`.

  - **Number:** A sequential number, starting from 04 and increasing in increments of 4.

  - **Example Chain IDs:**
    - `c04` - Represents the first defined chain in a BLOCK.

    - `c08` - Represents the second defined chain in the same BLOCK.

    - `c12` - Represents the third defined chain in the same BLOCK.

- **Microservice Identifier (`ub02130`):** Composed of an alphabetic prefix and a numeric suffix. The alphabetic prefix is constructed by concatenating the initial letter of each word comprising the full microservice name (e.g., `ub` for `user board`). The numeric suffix, a four or five digit number (e.g., `02130`), correlates to the specific Flow and BLOCK within the system where the microservice is originally defined.
  - `ub`: Indicates the event originated in the User Board (ub) microservice.

  - `02130`: A composite number providing contextual details:
    - `021`: Denotes the specific Flow within the ub microservice where the event occurred. (See the "Flows and BLOCKs" documentation for details on flows.)
    - `30`: Identifies the BLOCK within the flow where the event happened. BLOCKs group related functionalities within a flow.

- **Execution Order Number (`e05`):** Specifies the sequential execution order of a function within its BLOCK.
  - **Prefix:** `e`: Specifies the sequential execution order of a function within its Block

  - **Number:**`05`: This is the first execution of the function within BLOCK. Execution order numbers increment in multiples of 5 (`e05`, `e10`, `e15`, etc.)

  - **Example:** 
    - `e05`: for the first execution of the function within particular BLOCK. 
    - `e10`: for the second execution of the function within same BLOCK. 
    - `e15`: for the third execution of the function within same BLOCK.

- **PSN ID (`prn05`):**
  - Format: `psn` + number
  - Number: Uniquely identifies the data structure within the microservice function.
  - **For requests, PSN IDs start from 05 and increment by 4 (e.g., prn05, prn09, prn13).**
  - **For responses, PSN IDs start from 14 and increment by 4 (e.g., prn14, prn18, prn22).**
  
- **Data Type (`ugd`):** A categorization of data based on its origin and purpose:
  - `ugd`: User Generated Data
  - `ucd`: User Clicked Data
  - `sgd`: System Generated Data
  - `srd`: System Responded Data
  - `sed`: System Error Data

**Example: `c04-ub02130e05-prn05ugd`**

**`c04`**: Communication Chain ID

**`ub02130`**: Microservice ID

**`e05`**: Microservice Function Execution Number

**`prn05ugd`**: PRN ID (resource number 05 for user generated data)

#### Relationship Between PSN and PRN

- A PSN defines the structure of data, acting as a blueprint for the data format.
- A PRN references specific data instances that adhere to the structure defined by a corresponding PSN.
- Both PSN and PRN share the same communication chain, microservice, and function execution components, ensuring data consistency and traceability within the chain.

### **Segment Order**

| Segment   | Position | Rationale                                                    |
| --------- | -------- | ------------------------------------------------------------ |
| `c04`     | 1st      | **Communication Chain ID:** Placing it first establishes the overarching context for the data and facilitates grouping related PSNs and PRNs. |
| `ub02130` | 2nd      | **Microservice ID:** Following the Communication Chain ID, it narrows down the data's origin and processing stage. |
| `e05`     | 3rd      | **Microservice Function Execution Number:** Provides further granularity, allowing tracking of data flow within a microservice. |
| `prn05`   | 4th      | **PSN/PRN ID:** Placed after the context-defining segments, it focuses on the core identifier of the data. |
| `ugd`     | 5th      | **Data Type:** Placing it last provides additional metadata about the data, aiding in filtering and analysis. |



**Rationale for Segment Order**

The chosen order of segments is designed to optimize data processing, analysis, and traceability within the communication chain.

1. **Communication Chain ID:** Identifies the specific sequence of microservices involved in data processing.
   
2. **Microservice ID:** Specifies the particular microservice handling the data.
   
3. **Microservice Function Execution Number:** Indicates the specific function within the microservice that processes the data.
   
4. **PSN/PRN ID:** Uniquely identifies the data structure or instance within the specified context.
   
5. **Data Type:** Categorizes the data based on its origin and purpose.


**Benefits of the Segment Order**

- Efficient Data Retrieval: The order facilitates rapid filtering and retrieval of data based on various criteria.
  
- Improved Data Analysis: By grouping related data segments, analysis becomes more streamlined and informative.

- Enhanced Traceability: The ordered structure enables easy tracking of data Flow through the communication chain.

**Conclusion**

  The specific order of segments in PSN and PRN is fundamental for maintaining data consistency, enabling efficient processing, and supporting comprehensive analysis. Adherence to this standard ensures optimal performance and understanding of the data within the Sambar Web Application.
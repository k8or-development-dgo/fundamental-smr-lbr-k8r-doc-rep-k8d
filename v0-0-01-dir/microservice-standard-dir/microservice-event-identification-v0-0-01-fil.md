## Microservice Event ID Numbering Convention within the Sambar/LeBar/k8or Web Applications

This document outlines the structure and purpose of Event IDs within the Sambar/LeBar/k8or web applications. It provides a detailed explanation of each segment within the Event ID and its significance in identifying the source, context, and sequence of events.

## Content

1. **[Introduction](#Introduction)**
2. **[Event ID Format](#Event-ID-Format)**
3. **[Key Points](#Key-Points)**
4. **[Importance of Event ID Segment Order](#Importance-of-Event-ID-Segment-Order)**
5. **[Key Benefits of the Segment Order](#Key-Benefits-of-the-Segment-Order)**
6. **[Document Metadata](#Document-Metadata)**

<h1 id="Introduction">Introduction</h1>

Event IDs are structured identifiers that uniquely describe actions within the Sambar/LeBar/k8or microservice ecosystem. Each Event ID is composed of several numerical segments, each conveying specific information about the event's context and location within the system:

<h1 id="Event-ID-Format">Event ID Format</h1>

**`ub02130m03f04e05post` Numbering Segments Explanation**

1. **Microservice Identifier `ub02130`:** 
    * Composed of an alphabetic prefix and a numeric suffix. The alphabetic prefix is constructed by concatenating the initial letter of each word comprising the full microservice name `ub` for `user board`. The numeric suffix, a four or five digit number `02130`, correlates to the specific Flow and BLOCK within the system where the microservice is originally defined.
        * `ub`: Indicates the event originated in the User Board (ub) TypeScript Angular frontend microservice.
        * `02130`: A composite number providing contextual details:
          * `021`: Denotes the specific Flow within the ub microservice where the event occurred.
          * `30`: Identifies the BLOCK within the flow where the event happened. BLOCKs group related functionalities within a flow.
2. **Microservice Sequence Number `m03`:** 
    * A two-digit number prefixed with `m` indicating the sequence of the microservice within a BLOCK.
        * `m`: Designates that the number pertains to the microservice sequence.
        * `03`: This event originated in the first microservice within the specified BLOCK.
        * Microservice sequence numbers increment in multiples of 3 `m03`, `m06`, `m09`, etc.
    * **Example:** 
        * `m03`: for the first microservice in this particular BLOCK. 
        * `m06`: for the second microservice in the same BLOCK. 
        * `m09`: for the third microservice in the same BLOCK.
4. **Function Sequence Number `f04`:** 
    * A two-digit number prefixed with `f` indicating the sequence of the function within a microservice.
        * `f`: Indicates that the number pertains to the function sequence within the microservice.
        * `04`: This event originated in the first function of the microservice.
        * Function sequence numbers increment in multiples of 4 `f04`, `f08`, `f12`, etc.
    * **Example**: 
        * `f04`: for the first function of the particular microservice. 
        * `f08`: for the second function of the same microservice. 
        * `f12`: for the third function of the same microservice.
5. **Execution Order Number `e05`:** 
    * Specifies the sequential execution order of a function within its BLOCK.
        * `e`: Specifies the sequential execution order of a function within its Block
        * `05`: This is the first execution of the function within BLOCK.
        * Execution order numbers increment in multiples of 5 `e05`, `e10`, `e15`, etc.
    * **Example**: 
        * `e05`: for the first execution of the function within particular BLOCK. 
        * `e10`: for the second execution of the function within same BLOCK. 
        * `e15`: for the third execution of the function within same BLOCK.
6. **HTTP Method `post`:** 
    * A three or four letter code indicating the HTTP method used to trigger the event. 
    * The final segment indicates the HTTP method used to trigger the event `post` or `get`.
7. **Example Interpretation:**
    * Given the Event ID `ub02130m03f04e05post`, we can deduce the following:
    * This is an event from the User-Board `ub` microservice.
    * It occurred within flow 021 and BLOCK 30.
    * It was triggered by the first function `f04` in the first microservice `m03` of that BLOCK.
    * This is the first execution `e05` of that function.
    * The HTTP method used was `post`.

<h1 id="Key-Points">Key Points</h1>

* Unique Identification: Event IDs provide a precise and unique way to track actions within the microservice ecosystem.
* Contextual Information: The embedded numbering scheme offers valuable context about where and how events occur.
* Debugging and Analysis: Event IDs are invaluable for debugging, performance analysis, and understanding user interactions with the system.

<h1 id="Importance-of-Event-ID-Segment-Order">Importance of Event ID Segment Order</h1>

The specific order of segments in the Event ID `ub02130m03f04e05post` is critical for ensuring clarity, efficient searching, and logical organization of event data. Let's delve into why each segment occupies its designated position:

- **Microservice Identifier `ub02130`:**
  - Position: First
  - Rationale: The microservice identifier is the most general piece of information, identifying the origin of the event. Placing it first allows for immediate filtering and grouping of events based on the source microservice. This is especially useful when dealing with a large number of microservices within a system.

- **Microservice Sequence Number `m03`:**
  - Position: Second
  - Rationale: After identifying the microservice, the next logical step is to determine which specific instance (or sequence) of that microservice generated the event. This placement allows for further narrowing down of the event's origin within the microservice ecosystem.

- **Function Sequence Number `f04`:**
  - Position: Third
  - Rationale: Once the microservice and its sequence are known, the function sequence number pinpoints the precise function responsible for the event. This logical progression from broader to narrower context aids in understanding the event's location within the codebase.

- **Execution Order Number `e05`:**
  - Position: Fourth
  - Rationale: The execution order number provides temporal context, indicating the chronological sequence of the function's executions. By placing it after the function identifier, it naturally groups multiple executions of the same function together, making it easier to track their sequence and identify potential issues.

- **HTTP Method `post`:**
  - Position: Fifth (Last)
  - Rationale: The HTTP method is the most specific detail about the event, describing the action performed. Placing it at the end serves as a quick reference for the type of operation involved. Additionally, it allows for flexible filtering based on the HTTP method without affecting the core identification of the event's source and context.

<h1 id="Key-Benefits-of-the-Segment-Order">Key Benefits of the Segment Order</h1>

- **Hierarchical Filtering:** The order allows for efficient filtering at various levels of granularity, from the microservice level down to the specific function execution.
- **Logical Progression:** The order mirrors the logical flow of event generation, progressing from the broadest context to the most specific details.
- **Readability and Interpretability:** The structured order makes Event IDs easier to read and interpret, even for those unfamiliar with the system's intricacies.

---

<h2 id="Document-Metadata-Naming-Convention">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Microservice Event ID Numbering Convention within the Sambar/LeBar/k8or Web Applications |
| | Description | This document outlines the structure and purpose of Event IDs within the Sambar/LeBar/k8or web applications. It provides a detailed explanation of each segment within the Event ID and its significance in identifying the source, context, and sequence of events. |
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
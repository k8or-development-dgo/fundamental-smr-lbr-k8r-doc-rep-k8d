## Request Payload Naming and Numbering Convention within the Sambar/LeBar/k8or Web Applications

This document offers a comprehensive technical analysis of the structure and conventions employed within request payloads in the Sambar/LeBar/k8or web applications, specifically focusing on the `metadataOBJ` and `actualDataOBJ` components.

## Content

1. **[Example Request Payload](#Example-Request-Payload)**
2. **[Metadata Object `metadataOBJ`](#Metadata-Object-metadataOBJ)**
3. **[Metadata Object `actualDataOBJ`](#Metadata-Object-actualDataOBJ)**
4. **[Example Structure Based on the Provided Payload](#Example-Structure-Based-on-the-Provided-Payload)**
5. **[Adaptability to Diverse Request Types](#Adaptability-to-Diverse-Request-Types)**
6. **[Naming Conventions](#Naming-Conventions)**
7. **[Numbering Considerations](#Numbering-Considerations)**
8. **[Order of Elements](#Order-of-Elements)**
9. **[Document Metadata](#Document-Metadata)**

<h1 id="Example-Request-Payload">Example Request Payload</h1>

```json
{
  "metadataOBJ": {
    "eventIDKEY": "ub02130m03f16e20post",
    "psnKEY": "c16-ub02130e20-psn05ugd",
    "prnKEY": "c16-ub02130e20-prn05ugd",
    "actionTypeKEY": "lebar-withdraw",
    "eventTypeKEY": "assign-lebar-withdraw-reference-code",
    "persistDataStatusKEY": true,
    "recordEventStatusKEY": false
  },
  "actualDataOBJ": { 
    "eventIDKEY": "ub02130m03f16e20post",
    "usernameKEY": "james.born",
    "accountNumberKEY": "3683974753754359"
  }
}
```

<h1 id="Metadata-Object-metadataOBJ">Metadata Object `metadataOBJ`</h1>

The `metadataOBJ` is a standardized component included in all request payloads within the Sambar Web Application. It serves as a repository for essential metadata, providing context and instructions for payload processing.

- `eventIDKEY`: A unique identifier for the event, ensuring traceability and distinction.
- `psnKEY`: The Payload Structure Number (PSN), defining the structural blueprint of the payload's data.
- `prnKEY`: The Payload Resource Number (PRN), uniquely identifying this specific instance of the payload data.
- `actionTypeKEY`: Categorizes the action associated with the payload (e.g., `lebar-withdraw`, `lebar-purchase`).
- `eventTypeKEY`: Describes the specific type of event represented by the payload, offering further granularity.
- `persistDataStatusKEY`: A boolean flag indicating whether the payload's data should be stored persistently.
- `recordEventStatusKEY`: A boolean flag dictating whether the event itself should be logged or recorded.

The consistent structure of the `metadataOBJ` across all request payloads promotes predictability and simplifies processing logic.

<h1 id="Metadata-Object-actualDataOBJ">Metadata Object `actualDataOBJ`</h1>

The `actualDataOBJ` encapsulates the core data pertinent to the request. In contrast to the standardized `metadataOBJ`, the structure and content within the `actualDataOBJ` are highly dynamic, adapting to the specific requirements of each request type. This flexibility enables the system to handle a wide array of business use cases.

<h1 id="Example-Structure-Based-on-the-Provided-Payload">Example Structure Based on the Provided Payload</h1>

- `eventIDKEY`: The unique event identifier, mirroring the one in `metadataOBJ` for cross-referencing.
- `usernameKEY`: The username relevant to the request, potentially used for authentication or authorization.
- `accountNumberKEY`: The account number associated with the request, crucial for financial transactions or data retrieval.

<h1 id="Adaptability-to-Diverse-Request-Types">Adaptability to Diverse Request Types</h1>

While the example showcases specific keys, the `actualDataOBJ` is designed to accommodate varying structures.

- A payment request might include:
  - `amountKEY`
  - `currencyKEY`
  - `recipientDetailsOBJ` (potentially containing nested keys like `name`, `address`, etc.)
- A user registration request might encompass:
  - `usernameKEY`
  - `emailKEY`
  - `passwordKEY`
  - `personalInformationOBJ` (potentially containing `firstName`, `lastName`, `dateOfBirth`, etc.)

<h1 id="Naming-Conventions">Naming Conventions</h1>

- **Key-based Naming:** Both `metadataOBJ` and `actualDataOBJ` utilize key-based naming for properties, enhancing clarity and consistency.
- **CamelCase:** Property names adhere to camelCase formatting (e.g., `eventIDKEY`, `usernameKEY`) to improve readability.
- **Suffix `OBJ`**: The suffix 'KEY' is appended to property names to explicitly denote them as objects within the JSON structure.
- **Suffix `KEY`**: The suffix 'KEY' is appended to property names to explicitly denote them as keys within the JSON structure.

<h1 id="Numbering-Considerations">Numbering Considerations</h1>

- **Event ID (`eventIDKEY`)**: A unique identifier, potentially incorporating sequential numbering or timestamp-based generation for distinction and traceability.
- **PSN and PRN:** These numbers follow established conventions, as elaborated in prior documentation, to ensure precise identification of payload structures and instances.
- **Array Indices:** When arrays are present within the payload, they are indexed numerically, starting from 0, to enable orderly access to their elements.

<h1 id="Order-of-Elements">Order of Elements</h1>

While JSON object element order doesn't inherently affect functionality, maintaining consistency aids readability and comprehension.

#### Within `metadataOBJ`

- `eventIDKEY` is often placed first for immediate identification.
- `psnKEY` and `prnKEY` follow to provide structural and instance context.
- `actionTypeKEY` and `eventTypeKEY` describe the payload's intent and nature.
- `persistDataStatusKEY` and `recordEventStatusKEY` are often positioned last as metadata about payload handling.

#### Within `actualDataOBJ`

- **Core data elements** are generally placed at the beginning for prominence.
- **Related data groups** are often clustered together for logical organization.
- **Optional data** tends to be positioned towards the end.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Request Payload Naming and Numbering Convention within the Sambar/LeBar/k8or Web Applications |
| | Description | This document offers a comprehensive technical analysis of the structure and conventions employed within request payloads in the Sambar/LeBar/k8or Web Application, specifically focusing on the `metadataOBJ` and `actualDataOBJ` components. |
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
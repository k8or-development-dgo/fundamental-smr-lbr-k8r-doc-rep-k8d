# Response Payload Naming and Numbering Convention within the Sambar/LeBar/k8or Web Applications

This document offers a comprehensive technical analysis of the structure and conventions employed within response payloads in the Sambar/LeBar/k8or web application, specifically focusing on the `metadataOBJ` and `actualDataOBJ` components.

## Content

1. **[Successful Response Example Payload](#Successful-Response-Example-Payload)**
2. **[Error Response Example Payload](#Error-Response-Example-Payload)**
3. **[Actual Data Object `actualDataOBJ`](#Metadata-Object-metadataOBJ)**
4. **[Naming Conventions](#Naming-Conventions)**
5. **[Numbering Considerations](#Numbering-Considerations)**
6. **[Order of Elements](#Order-of-Elements)**
7. **[Conclusion](#Conclusion)**
8. **[Document Metadata](#Document-Metadata)**

<h1 id="Successful-Response-Example-Payload">Successful Response Example Payload</h1>

```json
{
  "metadataOBJ": {
    "eventIDKEY": "ub02130m03f16e20post",
    "psnKEY": "c16-ub02130e20-psn18sgd",
    "prnKEY": "c16-ub02130e20-prn18sgd"
  },
  "actualDataOBJ": { 
    "eventIDKEY": "rc0615m06f04e20post",
    "statusKEY": true,
    "referenceCodeKEY": "ugGJaG687d5FGkJh"
  }
}
```

<h1 id="Error-Response-Example-Payload">Error Response Example Payload</h1>

```json
{
  "metadataOBJ": {
    "eventIDKEY": "ub02130m03f16e20post",
    "psnKEY": "c16-ub02130e20-psn18sgd",
    "prnKEY": "c16-ub02130e20-prn18sgd"
  },
  	"actualDataOBJ": { 
  	"eventIDKEY": "ub02130m03f16e20post",
    "statusKEY": false,
  	"errorCodeKEY": "ub02130-cls003fun16",
  	"messageKEY": "This is a sample error message."
  }
}
```

<h1 id="Metadata-Object-metadataOBJ">Metadata Object `metadataOBJ`</h1>

The `metadataOBJ` is a standardized component present in response payloads. It provides crucial metadata for context and traceability, linking the response to the original request.

- `eventIDKEY`: Uniquely identifies the response and correlates it to the initiating request.
- `psnKEY`: The Payload Structure Number, defining the response data structure. It may differ from the request's PSN if the response structure changes significantly.
- `prnKEY`: The Payload Resource Number, uniquely identifying this specific response data instance. It might also differ from the request's PRN if the response structure changes.

The `metadataOBJ` maintains consistency across most responses, aiding predictability and client-side processing. However, it might be omitted in specific scenarios like error responses for brevity or specialized handling.

<h1 id="Actual-Data-Object-actualDataOBJ">Actual Data Object `actualDataOBJ`</h1>

The `actualDataOBJ` encapsulates the core data returned in response to the request. Its structure is flexible, adapting to the request type and expected response data.

## Example Structures

1. **Successful Response**
- `eventIDKEY`: A unique identifier for the response event, useful for server-side logging and analysis.
- `statusKEY`: A boolean indicating success `true` or failure `false` of the request.
- `referenceCodeKEY`: A unique code referencing the performed operation or transaction.

2. **Error Response**
- `eventIDKEY`: The unique event identifier, included for traceability even in error scenarios.
- `statusKEY`: A boolean indicating the failure status `false`.
- `errorCodeKEY`: A coded identifier specifying the error that occurred.
- `messageKEY`: A human-readable error message, potentially offering guidance for resolution.

3. **Adaptability**
- The `actualDataOBJ` is designed to handle various response types, including:
    - Successful responses with transaction IDs, confirmation messages, or requested data.
    - Error responses with error codes and descriptive messages.

<h1 id="Naming-Conventions">Naming Conventions</h1>

- **Key-based Naming:** Properties use key-based naming for clarity and consistency.
- **CamelCase:** Property names follow camelCase formatting for readability.
- **Suffix `OBJ`**: The suffix 'OBJ' designates objects within the JSON structure.
- **Suffix `KEY`**: The suffix 'KEY' designates keys within the JSON structure.

<h1 id="Numbering-Considerations">Numbering Considerations</h1>

- **`eventIDKEY`**: Often mirrors the request's `eventIDKEY` for traceability.
- **`psnKEY` and `prnKEY`**: Usually derived from the request payload but may differ if the response structure changes significantly.

<h1 id="Order-of-Elements">Order of Elements</h1>

While JSON object element order isn't functionally critical, adhering to conventions enhances readability and maintainability.

#### Within `metadataOBJ` 

- `eventIDKEY`: Placed first for immediate context.
- `psnKEY`: Follows to provide structural information.
- `prnKEY`: Concludes the metadata with the data instance reference.

#### Within `actualDataOBJ`

- **Status indicators** (`statusKEY` or `errorCodeKEY`) are often placed first.
- **Core data elements** directly related to the response follow.
- **Additional information** like error messages or metadata can be included last.

<h1 id="Conclusion">Conclusion</h1>

Response payloads in the Sambar/LeBar/k8or web applications follow a structured approach with clear naming and numbering conventions. The `metadataOBJ`, when present, provides context and traceability. The `actualDataOBJ` flexibly accommodates diverse response data, including error scenarios, with the inclusion of the `statusKEY` to clearly indicate the outcome of the request. Adhering to these conventions fosters code maintainability, readability, and efficient processing.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Response Payload Naming and Numbering Convention within the Sambar/LeBar/k8or Web Applications |
| | Description | This document offers a comprehensive technical analysis of the structure and conventions employed within response payloads in the Sambar/LeBar/k8or web application, specifically focusing on the `metadataOBJ` and `actualDataOBJ` components. |
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
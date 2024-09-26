## Response Payload Naming and Numbering Process

This document offers a comprehensive technical analysis of the structure and conventions employed within response payloads in the Sambar Web Application, specifically focusing on the `metadataOBJ` and `actualDataOBJ` components.

### Example Successful Response Payload

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

### Example Error Response Payload

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

### Metadata Object (`metadataOBJ`)

The `metadataOBJ` is a standardized component present in response payloads. It provides crucial metadata for context and traceability, linking the response to the original request.

- `eventIDKEY`: Uniquely identifies the response and correlates it to the initiating request.
- `psnKEY`: The Payload Structure Number, defining the response data structure. It may differ from the request's PSN if the response structure changes significantly.
- `prnKEY`: The Payload Resource Number, uniquely identifying this specific response data instance. It might also differ from the request's PRN if the response structure changes.

The `metadataOBJ` maintains consistency across most responses, aiding predictability and client-side processing. However, it might be omitted in specific scenarios like error responses for brevity or specialized handling.

### Actual Data Object (`actualDataOBJ`)

The `actualDataOBJ` encapsulates the core data returned in response to the request. Its structure is flexible, adapting to the request type and expected response data.

#### Example Structures

##### Successful Response

- `eventIDKEY`: A unique identifier for the response event, useful for server-side logging and analysis
- `statusKEY`: A boolean indicating success (`true`) or failure (`false`) of the request
- `referenceCodeKEY`: A unique code referencing the performed operation or transaction

##### Error Response

- `eventIDKEY`: (Optional) The unique event identifier, included for traceability even in error scenarios
- `statusKEY`: A boolean indicating the failure status (`false`)
- `errorCodeKEY`: A coded identifier specifying the error that occurred
- `messageKEY`: A human-readable error message, potentially offering guidance for resolution

#### Adaptability

The `actualDataOBJ` is designed to handle various response types, including:

- Successful responses with transaction IDs, confirmation messages, or requested data
- Error responses with error codes and descriptive messages

### Naming Conventions

- **Key-based Naming:** Properties use key-based naming for clarity and consistency.
- **CamelCase:** Property names follow camelCase formatting for readability
- **Suffix `OBJ`**: The suffix 'OBJ' designates objects within the JSON structure
- **Suffix `KEY`**: The suffix 'KEY' designates keys within the JSON structure

### Numbering Considerations

- **`eventIDKEY`**: Often mirrors the request's `eventIDKEY` for traceability
- **`psnKEY` and `prnKEY`**: Usually derived from the request payload but may differ if the response structure changes significantly

### Order of Elements

While JSON object element order isn't functionally critical, adhering to conventions enhances readability and maintainability.

#### Within `metadataOBJ` 

- `eventIDKEY`: Placed first for immediate context
- `psnKEY`: Follows to provide structural information
- `prnKEY`: Concludes the metadata with the data instance reference

#### Within `actualDataOBJ`

- **Status indicators** (`statusKEY` or `errorCodeKEY`) are often placed first
- **Core data elements** directly related to the response follow
- **Additional information** like error messages or metadata can be included last

### Conclusion

Response payloads in the Sambar Web Application follow a structured approach with clear naming and numbering conventions. The `metadataOBJ`, when present, provides context and traceability. The `actualDataOBJ` flexibly accommodates diverse response data, including error scenarios, with the inclusion of the `statusKEY` to clearly indicate the outcome of the request. Adhering to these conventions fosters code maintainability, readability, and efficient processing.
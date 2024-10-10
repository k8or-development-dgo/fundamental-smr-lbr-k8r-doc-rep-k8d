## Request Payload Naming and Numbering Process

This document offers a comprehensive technical analysis of the structure and conventions employed within request payloads in the Sambar Web Application, specifically focusing on the `metadataOBJ` and `actualDataOBJ` components.

### Example Request Payload

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

### Metadata Object (`metadataOBJ`)

The `metadataOBJ` is a standardized component included in all request payloads within the Sambar Web Application. It serves as a repository for essential metadata, providing context and instructions for payload processing.

- `eventIDKEY`: A unique identifier for the event, ensuring traceability and distinction.
- `psnKEY`: The Payload Structure Number (PSN), defining the structural blueprint of the payload's data.
- `prnKEY`: The Payload Resource Number (PRN), uniquely identifying this specific instance of the payload data.
- `actionTypeKEY`: Categorizes the action associated with the payload (e.g., `lebar-withdraw`, `lebar-purchase`).
- `eventTypeKEY`: Describes the specific type of event represented by the payload, offering further granularity.
- `persistDataStatusKEY`: A boolean flag indicating whether the payload's data should be stored persistently.
- `recordEventStatusKEY`: A boolean flag dictating whether the event itself should be logged or recorded.

The consistent structure of the `metadataOBJ` across all request payloads promotes predictability and simplifies processing logic.

### Actual Data Object (`actualDataOBJ`)

The `actualDataOBJ` encapsulates the core data pertinent to the request. In contrast to the standardized `metadataOBJ`, the structure and content within the `actualDataOBJ` are highly dynamic, adapting to the specific requirements of each request type. This flexibility enables the system to handle a wide array of business use cases.

#### Example Structure Based on the Provided Payload

- `eventIDKEY`: The unique event identifier, mirroring the one in `metadataOBJ` for cross-referencing.
- `usernameKEY`: The username relevant to the request, potentially used for authentication or authorization.
- `accountNumberKEY`: The account number associated with the request, crucial for financial transactions or data retrieval.

#### Adaptability to Diverse Request Types

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

### Naming Conventions

- **Key-based Naming:** Both `metadataOBJ` and `actualDataOBJ` utilize key-based naming for properties, enhancing clarity and consistency.
- **CamelCase:** Property names adhere to camelCase formatting (e.g., `eventIDKEY`, `usernameKEY`) to improve readability.
- **Suffix `OBJ`**: The suffix 'KEY' is appended to property names to explicitly denote them as objects within the JSON structure.
- **Suffix `KEY`**: The suffix 'KEY' is appended to property names to explicitly denote them as keys within the JSON structure.

### Numbering Considerations

- **Event ID (`eventIDKEY`)**: A unique identifier, potentially incorporating sequential numbering or timestamp-based generation for distinction and traceability.
- **PSN and PRN:** These numbers follow established conventions, as elaborated in prior documentation, to ensure precise identification of payload structures and instances.
- **Array Indices:** When arrays are present within the payload, they are indexed numerically, starting from 0, to enable orderly access to their elements.

### Order of Elements

While JSON object element order doesn't inherently affect functionality, maintaining consistency aids readability and comprehension.

#### Within `metadataOBJ`

- `eventIDKEY` is often placed first for immediate identification.
- `psnKEY` and `prnKEY` typically follow to provide structural and instance context.
- `actionTypeKEY` and `eventTypeKEY` describe the payload's intent and nature.
- `persistDataStatusKEY` and `recordEventStatusKEY` are often positioned last as metadata about payload handling.

#### Within `actualDataOBJ`

- **Core data elements** are generally placed at the beginning for prominence.
- **Related data groups** are often clustered together for logical organization.
- **Optional data** tends to be positioned towards the end.

### Conclusion

The meticulous naming conventions and thoughtful structuring of request payloads, particularly within the `metadataOBJ` and `actualDataOBJ`, contribute significantly to the Sambar Web Application's robustness and maintainability. By adhering to these standards, developers ensure clarity, consistency, and efficiency in data exchange and processing.
# Sambar/LeBar/k8or Microservice Naming Convention

This document outlines the microservice naming convention used within the Sambar/LeBar/k8or web application. It provides a detailed explanation of each segment within the microservice name and its significance in identifying the microservice's purpose, context, and deployment environment.

## Content

1. **[Introduction](#Introduction)**
1. **[Breakdown of Segments](#Breakdown-of-Segments)**
1. **[Purpose of the Naming Convention](#Purpose-of-the-Naming-Convention)**
1. **[Order of Segments in Microservice Naming Convention](#Order-of-Segments-in-Microservice-Naming-Convention)**
1. **[Importance of the Order](#Importance-of-the-Order)**
1. **[Important Note](#Important-Note)**
7. **[Document Metadata](#Document-Metadata)**

<h1 id="Introduction">Introduction</h1>

Sambar/LeBar/k8or web applications employ a specific naming convention for microservices to ensure clarity, organization, and efficient management. The convention follows a structured format that incorporates essential information about the microservice.

<h1 id="Microservice-Name-Structure">Microservice Name Structure</h1>

A Sambar/LeBar/k8or web application microservice name consists of multiple segments separated by hyphens:

```
<Microservice Identifier>-<Subscription Plan>-<Country>-<Language>-<Environment>-<Region>
```
```
ub02130-no-us-en-sd2-lo
```

<h1 id="Breakdown-of-Segments">Breakdown of Segments</h1>

| Segment    | Description                                                  |
| ---------- | ------------------------------------------------------------ |
| `ub02130` | **Microservice Identifier**: Composed of an alphabetic prefix and a numeric suffix. The alphabetic prefix is constructed by concatenating the initial letter of each word comprising the full microservice name, `ub` for `user board`. The numeric suffix, a four or five digit number (e.g., `02130`), correlates to the specific Flow and BLOCK within the system where the microservice is originally defined. |
| `no`     | **Subscription Plan**: Specifies the target user group based on subscription plans, `no` for no subscription. |
| `us`     | **Country**: Indicates the geographical region for which the microservice is designed, `us` for the United States. |
| `en`     | **Language**: Specifies the language supported by the microservice, `en` for English. |
| `sd2`    | **Environment**: Identifies the operational environment, `sd2` for Sambar development environment. |
| `lo`      | **Region**: Specifies the region where the microservice is deployed, `lo` for London. |

<h1 id="Purpose-of-the-Naming-Convention">Purpose of the Naming Convention</h1>

The naming convention serves several key purposes:

- **Clarity and Understanding:** Provides a clear and concise description of the microservice's purpose and characteristics.
- **Organization:** Enables efficient categorization and grouping of microservices based on various criteria.
- **Management:** Facilitates microservice lifecycle management, including deployment, scaling, and monitoring.
- **Debugging and Troubleshooting:** Aids in identifying the specific microservice involved in issues.

<h1 id="Order-of-Segments-in-Microservice-Naming-Convention">Order of Segments in Microservice Naming Convention</h1>

| Segment    | Placement | Rationale                                                    |
| ---------- | --------- | ------------------------------------------------------------ |
| `ub02130` | 1st       | This segment uniquely identifies the microservice, including its type and internal reference. Placing it first establishes the core identity of the service. |
| `no`     | 2nd       | Following the microservice identifier, the subscription plan segment specifies the target user group. This order allows for easy grouping of microservices based on subscription plans. |
| `us`     | 3rd       | After specifying the target user group, indicating the geographical region helps in categorizing microservices based on location. This order facilitates management of region-specific functionalities. |
| `en`     | 4rd       | Following the country, the language segment defines the supported language. This sequence logically builds on the geographical targeting and specifies the user language preference. |
| `sd2`    | 5th       | The environment segment indicates the operational context of the microservice. Placing it after the language suggests that the environment might influence the language or regional aspects of the service. |
| `lo`      | 6th       | The region segment specifies the physical location of the microservice. Placing it at the end emphasizes the deployment location, differentiating between microservices with identical configurations but deployed in different regions. |

<h1 id="Importance-of-the-Order">Importance of the Order</h1>

The specific order of segments in the microservice naming convention offers several advantages:

- **Logical Grouping:** Microservices can be grouped based on subscription plans, countries, languages, environments, or regions for efficient management.
- **Search and Filtering:** The ordered structure facilitates searching and filtering for specific microservices based on various criteria.
- **Scalability:** As the system grows, new microservices can be added while maintaining a consistent naming structure.
- **Understanding:** The order provides a clear and intuitive way to understand the purpose and characteristics of a microservice at a glance.

<h1 id="Important-Note">Important Note</h1>

The environment ID for the Sambar/LeBar/k8or web applications must be a two- or three-character code commencing with the letter `s` for Sambar, `l` for LeBar and `k` for k8or, followed by a single letter designating the particular environment:	

- `d`: development	
- `t`: testing	
- `p`: production
- `s`: staging

---

<h2 id="Document-Metadata-Naming-Convention">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Definition of a Communication Chain (Chain) and its ID Structure |
| | Description | This document provides a comprehensive explanation of Communication Chains (Chains) and their corresponding Chain IDs within the Sambar/LeBar/k8or web applications. It outlines the structure and significance of Chain IDs, their role in data flow tracking, and their integration with Payload Structure Numbers (PSNs) and Payload Resource Numbers (PRNs). |
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
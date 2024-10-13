# Application Backend Microservice Breakdown within the Sambar/LeBar/k8or Web Applications

This document provides a comprehensive overview of the backend microservice application resources utilized within the Sambar/LeBar/k8or web applications. It outlines the types of repositories involved, the naming conventions employed, and the various microservice types that contribute to the application's functionality.

## Content

1. **[Microservice Application Repository Types](#Microservice-Application-Repository-Types)**
2. **[Naming Convention for Microservice Application Repositories](#Naming-Convention-for-Microservice-Application-Repositories)**
3. **[Microservice Types](#Microservice-Types)**
4. **[Document Metadata](#Document-Metadata)**

<h1 id="Microservice-Application-Repository-Types">Microservice Application Repository Types</h1>

1. **Source Code Repository:** Contains the source code for the backend microservice, used to build the Docker image.
2. **Resource Manifest Repository:** Defines the configuration and deployment details for the backend microservice, including the newly built Docker image.
3. **Test Repository:** Contains test cases and scripts to verify the functionality of the deployed microservice.

<h1 id="Naming-Convention-for-Microservice-Application-Repositories">Naming Convention for Microservice Application Repositories</h1>

The naming convention for the microservice application repositories within the Sambar/LeBar/k8or web applications adheres to a consistent structure, designed for clarity and organization:

* **flow-2:** Indicates that this resource belongs to the `User Registration` Flow-2 of the Sambar web application, signifying its functional context within the broader application.
* **ua0206:** Represents a unique identifier assigned to the backend microservice, ensuring its distinct identification within the system. This component consists of two parts:
  * **ua:** The alphabetic prefix is formed by concatenating the initial letter of each word in the full microservice name. In this case, `ua` stands for `User Authentication` This prefix provides a concise representation of the backend microservice's primary function.
  * **0206:** The numeric suffix, such as `0206`, serves as a reference to the specific Flow and BLOCK within the system where the backend microservice is originally defined. This correlation facilitates traceability and understanding of the backend microservice's origin and context.
* **no:** Specifies the target user group based on subscription plans. In this case, `no` indicates that the backend microservice is designed for users who do not have a subscription.
* **us:** Indicates the geographical region for which the backend microservice is intended. `us` signifies that the backend microservice is designed for the United States market.
* **en:** Specifies the language supported by the microservice. `en` indicates that the microservice is designed for English-speaking users.
* **sd2:** Identifies the operational environment where the microservice is deployed. `sd2` signifies the Sambar development environment, indicating that the backend microservice is currently in a development phase.
* **lo:** Specifies the region where the microservice is deployed. `lo` indicates that the microservice is deployed in the London region.
* **src-cod:** Denotes the source code, indicating that this component contains the programming code that defines the backend microservice's functionality.
* **php:** Specifies the programming language used to develop the backend microservice. `php` indicates that the source code is written in PHP.
* **rep:** Indicates that this component is a repository, a collection of files and directories that store the backend microservice's code, configuration, and other resources.
* **sd2:** Identifies the operational environment, `sd2` for Sambar development environment.
* **dgo:** Indicates the cloud provider, DigitalOcean, where the backend microservice is deployed.

<h1 id="Microservice-Types">Microservice Types</h1>

The Sambar/LeBar/k8or web application utilizes a diverse range of microservices to implement various functionalities. 

1. Sambar web applications's microservices:

* **Site Static Page** Frontend `ssp`
* **User Board** Frontend `ub`
* **User Authentication** `ua`
* **User Invitation** `ui`
* **Analyst Article CMS** `aac`
* **User Information Payload** `uip`
* **User SMS Notification** `usn`
* **Subscription** `sub`
* **User Payload Event Log** `upel`
* **Credit Total** `ct`
* **LeBar Total** `lt`
* **LeBar Cent Information** `lci`
* **Add LeBar Form** Frontend `alf`
* **Add LeBar** `al`
* **User Board Notification** `ubn`
* **Move LeBar** `ml`
* **Trade Order** `to`
* **T-Input UI** Frontend `tu`
* **T-Input Logic** `tl`
* **Authorization** `auth`
* **Strategy Search Data** `ssd`
* **Strategy Subscription Event Log** `ssel`
* **Trade Data** `td`
* **Group Trade Logic** `gtl`
* **Credit Distribution** `cd`
* **Strategy Data** `sd`
* **Convert Credit Event Log** `ccel`
* **Historic Chart** `hc`
* **Analyst Strategy Information** `asi`
* **Formula Historic Equity Outright** `fm-heo`
* **Historic Equity Data** `hed`
* **Formula Historic Equity Two Leg Spread** `fm-hetls`
* **Trade Data Verify** `tdv`
* **Historic Average** `ha`
* **Strategy Statistic** `ss`
* **Historic Future Data** `hfd`
* **Formula Historic Future Outright** `fm-hfo`
* **Formula Historic Future Two Leg Spread** `fm-hftls`
* **Formula Historic Future Equity Spread** `fm-hfes`

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Application Backend Microservice Breakdown within the Sambar/LeBar/k8or Web Applications |
| | Description | This document provides a comprehensive overview of the backend microservice application resources utilized within the Sambar/LeBar/k8or web applications. It outlines the types of repositories involved, the naming conventions employed, and the various microservice types that contribute to the application's functionality. |
| | Identification | TBD | |
| | Version | v0-0-01 | |
| | Format | md | |
| | Revision | This is the first version uploaded to the ChatBOT. |
| | Author | Anna/Barb.Rock |
| | Date | October 13, 2024 |
| Subject Metadata | Alias | TBD |
| |  Name | TBD |
| |  FQID | TBD |
| |  Version | s0-0-01 |
| |  Action | 000010 |
| hGraph Metadata | Alias | none |
| |  Name | none |
| |  FQID | none |
| |  Version | none |
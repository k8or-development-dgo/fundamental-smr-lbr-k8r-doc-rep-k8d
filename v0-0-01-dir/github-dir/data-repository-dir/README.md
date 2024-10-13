# Data Preparation Resource Breakdown within the Sambar/LeBar/k8or Web Applications

This document uses `User Registration` Flow-2 as an example to illustrate the data preparation resource breakdown. The same principles and processes apply to all other flows within the Sambar/LeBar/k8or web applications.

## Content

1. **[Application Resources vs. Data Resources](#Application-Resources-vs-Data-Resources)**
2. **[Relationship Between Data Resources and BLOCKs](#Relationship-Between-Data-Resources-and-BLOCKs)**
3. **[Data Resource Types](#Data-Resource-Types)**
    * **[Register Plan Data](#Register-Plan-Data)**
    * **[User Account Number Data](#User-Account-Number-Data)**
    * **[User Invitation Code Data](#User-Invitation-Code-Data)**
    * **[Wordpress Options Data](#Wordpress-Options-Data)**
4. **[Action Words](#Action-Words)**
5. **[Data Preparation Order](#Data-Preparation-Order)**
6. **[Data Resource Unique Identification](#Data-Resource-Unique-Identification)**
7. **[Document Metadata](#Document-Metadata)**

<h1 id="Application-Resources-vs-Data-Resources">Application Resources vs. Data Resources</h1>

Within the Sambar/LeBar/k8or web applications, it's critical to differentiate between application resources and data resources.

* **Application Resources:** These resources form the core building BLOCKs of the application's functionality. They encompass elements like databases, tables, and collections that enable the application to operate.
* **Data Resources:** While also essential, data resources are primarily focused on providing the metadata and data preparation necessary for the application to function effectively. 

**Key Differences**

* **Functionality:** Application resources directly contribute to the application's core functionalities, such as user interactions, data processing, and service delivery. Data resources support these functionalities by providing the necessary data and metadata.
* **Dependencies:** Application resources in some cases depend on data resources for their operation, as they rely on the data provided by these resources.

**Example:**

* **Application Resource:** A MySQL table that contains user invitation codes.
* **Data Resource:** A data file containing user invitation codes.

<h1 id="Relationship-Between-Data-Resources-and-BLOCKs">Relationship Between Data Resources and BLOCKs</h1>

* **Data Resources within BLOCKs:** Each data resource is associated with a specific BLOCK within a flow. This ensures that the resources are used in the correct context to achieve the desired functionality.

<h1 id="Data-Resource-Types">Data Resource Types</h1>

Data repositories within the Sambar/LeBar/k8or web applications contain the following types of resources:

<h2 id="Register-Plan-Data">Register Plan Data</h2>

* **Example resource name** is `register-plan-dat-0203-v0-0-01-fil.json`.
* **Purpose:** This JSON file serves as a source of truth for the frontend component, providing it with a list of available subscription plans that a new user can choose from during the registration process. This data empowers users to make informed decisions regarding their desired subscription level.
* **Learn More:** Visit the provided URL for a comprehensive guide to understanding and using `Register Plan Data` JSON structure effectively:
    * **[Register Plan Data Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/data-repository-dir/register-plan-data-dir)**
* **Understanding:** Explore this resource to gain deeper insights into how register plan data effectively communicates available subscription plans to the frontend, facilitating a smooth user experience during registration.

<h2 id="User-Account-Number-Data">User Account Number Data</h2>

* **Example resource name** is `user-account-number-dat-0203-v0-0-01-fil.csv`.
* **Purpose:** This CSV file acts as a repository for a pool of available account numbers. These numbers are assigned to new users during the registration process. This data streamlines account creation by ensuring a readily available pool of unique identifiers.
* **Learn More:** Visit the provided URL for a comprehensive guide to understanding and using `Register Plan Data` JSON structure effectively:
    * **[User Account Number Data Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/data-repository-dir/user-account-number-data-dir)**
* **Understanding:** Delve into this resource to comprehend how user account number data maintains a readily available pool of unique identifiers for assigning to new users, ensuring a seamless account creation process.

<h2 id="User-Invitation-Code-Data">User Invitation Code Data</h2>

* **Example resource name** is `user-invitation-code-dat-0209-v0-0-01-fil.csv`.
* **Purpose:** This CSV file acts as a repository for user invitation codes. During registration, the user-provided invitation code is validated against this data source. Additionally, upon successful registration, the corresponding invitation code is marked as used within the system. This data resource safeguards the integrity of the invitation system and prevents code reuse.
* **Learn More:** Visit the provided URL for a comprehensive guide to understanding and using `Register Plan Data` JSON structure effectively:
    * **[User Invitation Code Data Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/data-repository-dir/user-invitation-code-data-dir)**
* **Understanding:** Explore this resource to gain a deeper understanding of how user invitation code data facilitates the validation and management of invitation codes, ensuring a secure and controlled user invitation process.

<h2 id="Wordpress-Options-Data">Wordpress Options Data</h2>

* **Example resource name** is `wp-options-dat-0212-v0-0-01-fil.csv`.
* **Purpose:** This CSV file serves as a data source for the `wp_options` table within the WordPress MySQL database. This table is responsible for storing settings specific to individual plugins and themes, enabling customization and extension of WordPress functionalities. This data allows for tailored user experiences based on specific plugin and theme configurations.
* **Learn More:** Visit the provided URL for a comprehensive guide to understanding and using `Register Plan Data` JSON structure effectively:
    * **[Wordpress Options Data Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/data-repository-dir/wp-options-data-dir)**
* **Understanding:** Explore this resource to gain a deeper understanding of how WordPress options data empowers the application to leverage plugin and theme-specific settings, ultimately personalizing user experiences.

<h1 id="Action-Words">Action Words</h1>

* The word **use** indicates that an existing data resource, prepared in previous flows, is being utilized directly without requiring additional preparation or modification.
* The word **prepare** is used for the preparation of data required for the User Registration Flow-2. This includes data extraction and transformation.
* The word **test** is used for the testing of prepared data to ensure its accuracy, completeness, and compliance with the expected format and requirements. This involves unit tests, integration tests, and other validation methods.

<h1 id="Data-Preparation-Order">Data Preparation Order</h1>

When listing data resources within the data resource list, it's important to follow a specific order to maintain clarity and consistency:

**1. Start with the First Left Leg:** Begin with the leftmost leg within the BLOCK diagram. This leg represents the initial step in the flow's process.

**2. Bottom to Top:** Within each leg, list data resources starting from the bottom and moving upwards. This approach reflects the natural flow of data processing and dependencies within the leg.

**3. Left to Right:** If a leg has multiple parallel branches, list the resources from left to right. This follows the reading order and helps in understanding the sequence of data flow.

**Rationale:**

* **Dependency Tracking:** This ordering helps visualize the dependencies between data resources within a leg. Resources at the bottom are often foundational, while those at the top may depend on data from lower-level resources.
* **Clarity and Readability:** Organizing data resources in this manner enhances the readability and understanding of the data resource list, making it easier to follow the data flow and identify potential dependencies.

<h1 id="Data-Resource-Unique-Identification">Data Resource Unique Identification</h1>

Data resources within the Sambar/LeBar/k8or web applications follow a standardized naming convention for identification. For example, `flow-2-dat-2` consists of:

* **flow-2:** Indicates the specific `User Registration` Flow-2 within the Sambar web application.
* **dat:** Denotes the resource type as a data component.
* **2:** Represents the sequence of the resource within the flow.

Each data resource has a unique identifier that reflects its purpose and placement within the Sambar/LeBar/k8or applications. It's critical to adhere to this naming convention and maintain the established order of data resource preparation to ensure consistent and efficient operation of the web applications.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Data Preparation Resource Breakdown within the Sambar/LeBar/k8or Web Applications |
| | Description | This document uses `User Registration` Flow-2 as an example to illustrate the data preparation resource breakdown. The same principles and processes apply to all other flows within the Sambar/LeBar/k8or web applications. |
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
# Application Resource Breakdown within the Sambar/LeBar/k8or Web Applications

This document uses `User Registration` Flow-2 as an example to illustrate the application resource breakdown. The same principles and processes apply to all other flows within the Sambar/LeBar/k8or web applications.

## Content

1. **[Application Resources vs. Infrastructure Resources](#Application-Resources-vs-Infrastructure-Resources)**
2. **[Relationship Between Application Resources and BLOCKs](#Relationship-Between-Application-Resources-and-BLOCKs)**
3. **[Structure of Application Resource Lists](#Structure-of-Application-Resource-Lists)**
4. **[Importance of Listing Application Resources by Leg](#Importance-of-Listing-Application-Resources-by-Leg)**
5. **[Creating Application Resource Lists for New Flows](#Creating-Application-Resource-Lists-for-New-Flows)**
6. **[Application Resource Types](#Application-Resource-Types)**
    * **[MongoDB Collection](#MongoDB-Collection)**
    * **[Spaces Object Storage](#Spaces-Object-Storage)**
    * **[MySQL Table](#MySQL-Table)**
    * **[CloudWatch](#CloudWatch)**
    * **[S3 Bucket](#S3-Bucket)**
    * **[Cognito Pool](#Cognito-Pool)**
    * **[Backend Microservice](#Backend-Microservice)**
    * **[Frontend Microservice](#Frontend-Microservice)**
7. **[Action Words](#Action-Words)**
8. **[Application Creation Order](#Application-Creation-Order)**
9. **[Action Words `Create` vs. `Test`](#Action-Words-Create-vs-Test)**
10. **[Application Resource Unique Identification](#Application-Resource-Unique-Identification)**
11. **[Document Metadata](#Document-Metadata)**

<h1 id="Application-Resources-vs-Infrastructure-Resources">Application Resources vs. Infrastructure Resources</h1>

It's important to note that application resources and infrastructure resources are distinct entities within the Sambar web application.

* **Infrastructure Resources:** These are specific resources used within individual flows of the application. They include Kubernetes clusters, namespaces, secrets, databases, cloud storage, and other essential components.
* **Application Resources:** These are specific resources used within individual BLOCKs of the application. They represent the building BLOCKs of the application's functionality, such as microservices, databases, tables, and collections.

<h1 id="Relationship-Between-Application-Resources-and-BLOCKs">Relationship Between Application Resources and BLOCKs</h1>

* **Application Resources within BLOCKs:** Each application resource is associated with a specific BLOCK within a flow. This ensures that the resources are used in the correct context to achieve the desired functionality.
* **Infrastructure Resources for the Flow:** While application resources are tied to individual BLOCKs, infrastructure resources support the entire flow. They provide the necessary foundation for all BLOCKs to operate seamlessly.

<h1 id="Structure-of-Application-Resource-Lists">Structure of Application Resource Lists</h1>

* **BLOCK-Based Organization:** Application resource lists are organized by BLOCK. Each BLOCK represents a distinct functional unit within a flow.
* **BLOCK Diagrams:** Each BLOCK has its own BLOCK diagram, visually illustrating the relationships between the application resources within that BLOCK.
* **Legs and Resources:** Within a BLOCK, there are multiple legs, each representing a specific aspect of the BLOCK's functionality. Legs are connected to backend resources and frontend/backend microservices.

<h1 id="Importance-of-Listing-Application-Resources-by-Leg">Importance of Listing Application Resources by Leg</h1>

* **Complete Functionality Representation:** To accurately depict the functional process, it's essential to list application resources based on their corresponding legs. This ensures that all necessary resources for each leg are included.
* **Resource Re-use:** Even if backend resources are used across multiple legs, listing them individually for each leg provides clarity and ensures that the complete functionality is represented.

<h1 id="Creating-Application-Resource-Lists-for-New-Flows">Creating Application Resource Lists for New Flows</h1>

When creating an application resource list for a new flow, follow these steps:

1. **Identify BLOCK Diagrams:** Locate all existing Lucidchart or Miro BLOCK diagrams that pertain to the new flow.
2. **Count BLOCKs:** Determine the number of BLOCKs within the flow based on the BLOCK diagrams.
3. **Find Flow Repository:** Locate the BLOCK diagrams for the new flow within the application repository.
4. **Start with the First BLOCK:** Begin with the initial BLOCK and include its BLOCK diagram URL.
5. **List Legs:** Identify and list all the legs within the BLOCK.
6. **List Application Resources:** For each leg, list the corresponding application resources.
7. **Resource Order:** **Start listing resources** from the **bottom left leg**, moving **from bottom to top and left to right**.
8. **Resource Types:**
    * **Backend Resources:** Begin with backend resources like MySQL tables, Spaces object storage, or MongoDB collections.
    * **Backend Microservices:** List backend microservices that interact with the backend resources.
    * **Frontend Microservices:** Include frontend microservices that communicate with the backend microservices.
    * **Infrastructure Resources:** Exclude IAM roles, policies, users, and access keys from the application resource list, as they are infrastructure-level resources.
9. **Infrastructure Resource References:** For infrastructure resources used in the application resource list, such as AWS Cognito, AWS SNS, AWS SES, AWS S3 bucket, AWS MySQL cluster or DigitalOcean MongoDB cluster, use the action words `test` and `use` and refer to the relevant infrastructure repositories.
10. **Essential Infrastructure Resources:** Include infrastructure resources that directly impact the application's functionality in the application resource list.

<h1 id="Application-Resource-Types">Application Resource Types</h1>

Application repositories within the Sambar/LeBar/k8or web applications contain the following types of resources:

<h2 id="MongoDB-Collection">MongoDB Collection</h2>

* **Example resource name** is `constant-0203-cll`.
* **Purpose:** Stores unstructured or semi-structured data in a flexible format, making it ideal for applications that require rapid data changes or complex queries.
* **Learn More:** Visit the provided URL for a comprehensive guide to understanding and using MongoDB collections effectively:
    * **[MongoDB Collection Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/application-repository-dir/mongodb-collection-dir)**
* **Understanding:** Explore how MongoDB collections store documents, support indexing for efficient querying, and provide features like aggregation pipelines and geospatial queries.

<h2 id="Spaces-Object-Storage">Spaces Object Storage</h2>

* **Example resource name** is `user-registration-image-03203-sd2-dgo`.
* **Purpose:** Stores files and objects of any size, offering durability, availability, and scalability. It's suitable for storing images, videos, documents, and other media assets.
* **Learn More:** Visit the provided URL for detailed information on managing object storage using Spaces:
    * **[Spaces Object Storage Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/application-repository-dir/space-object-storage-dir)**
* **Understanding:** Explore how to create Spaces buckets, upload and download objects, manage access controls, and integrate Spaces with other DigitalOcean services.

<h2 id="MySQL-Table">MySQL Table</h2>

* **Example resource name** is `user-account-number-0203`.
* **Purpose:** Stores structured data in a relational format, making it ideal for applications that require well-defined data relationships and complex queries.
* **Learn More:** Visit the provided URL for information on working with MySQL tables:
    * **[MySQL Table Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/application-repository-dir/mysql-table-dir)**
* **Understanding:** Explore how to create tables, define data types, establish relationships between tables, and execute SQL queries to retrieve and manipulate data.

<h2 id="CloudWatch">CloudWatch</h2>

* **Example resource name** is `DirectPublishToPhoneNumber`.
* **Purpose:** Monitors application metrics, logs, and events to gain insights into performance, identify issues, and optimize resource utilization.
* **Learn More:** Visit the provided URL for a detailed guide on using CloudWatch for application monitoring:
    * **[CloudWatch Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/application-repository-dir/cloudwatch-dir)**
* **Understanding:** Explore how to create CloudWatch dashboards, define metrics, set alarms, and analyze log data to troubleshoot and optimize your applications.

<h2 id="S3 Bucket">S3 Bucket</h2>

* **Example resource name** is `sms-sns-log-01603-sd2-aws`.
* **Purpose:** Stores files and objects of any size, offering durability, availability, and scalability. It's suitable for storing images, videos, documents, and other media assets.
* **Learn More:** Visit the provided URL for a deep dive into using S3 buckets for object storage:
    * **[S3 Bucket Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/application-repository-dir/s3-bucket-dir)**
* **Understanding:** Explore how to create S3 buckets, manage access controls, upload and download objects, and integrate S3 with other AWS services.

<h2 id="Cognito Pool">Cognito Pool</h2>

* **Example resource name** is `user-pool-03603-sd2-aws`.
* **Purpose:** Manages user identities, handles authentication and authorization, and provides features like multi-factor authentication and social login.
* **Learn More:** Visit the provided URL for understanding and using Cognito user pools for secure authentication:
    * **[Cognito Pool Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/application-repository-dir/cognito-pool-dir)**
* **Understanding:** Explore how to create Cognito user pools, configure sign-up and sign-in flows, integrate with other AWS services, and manage user attributes and permissions.

<h2 id="Backend-Microservice">Backend Microservice</h2>

* **Example resource name** is `ua0203-no-us-en-sd2-lo`.
* **Purpose:** Handles business logic, data processing, and API endpoints for the application. It can be built using various programming languages and frameworks.
* **Learn More:** Visit the provided URL for a comprehensive overview of the backend microservices architecture approach:
    * **[Backend Microservice Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/application-repository-dir/backend-microservice-dir)**
* **Understanding:** Explore the benefits of microservices architecture, design patterns, and best practices for building and managing microservices.

<h2 id="Frontend-Microservice">Frontend Microservice</h2>

* **Example resource name** is `ub02130-no-us-en-sd2-lo`.
* **Purpose:** Renders the user interface, handles user interactions, and communicates with backend microservices to fetch and display data.
* **Learn More:** Visit the provided URL for a comprehensive overview of the frontend microservices architecture approach:
    * **[Frontend Microservice Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/application-repository-dir/frontend-microservice-dir)**
* **Understanding:** Explore frontend technologies like HTML, CSS, JavaScript, and frameworks like React or Angular, as well as best practices for building user-friendly and responsive interfaces.

<h1 id="Action-Words">Action Words</h1>

* **Use:** Utilizes an existing resource created in prior flows.
* **Create:** Establishes new resources like databases, tables, or collections.
* **Build:** Compiles and packages the source code into a Docker image for deployment.
* **Deploy:** Makes the microservice operational by deploying its Docker image.
* **Test:** Verifies the functionality and proper operation of the created resources.

<h1 id="Infrastructure-Creation-Order">Infrastructure Creation Order</h1>

The infrastructure resource creation order is:

1. **Kubernetes Cluster:** Create the cluster first.
2. **Kubernetes Namespaces:** Create namespaces within the cluster for logical isolation.
3. **Kubernetes Secrets:** Create secrets for credentials and certificates.
4. **Ingress:** Configure the Ingress resource to route traffic to microservices.
5. **AWS Services:** Configure and test AWS services like SNS, SES, and Cognito.
6. **Storage:** Create storage buckets for data and images.
7. **IAM:** Create IAM policies, roles, and users with necessary permissions.

**Remember:** The specific order and resource requirements may vary depending on the flow and its functionalities. This breakdown provides a general guideline for understanding the infrastructure setup within Sambar/LeBar/k8or web applications.

<h1 id="Action-Words-Create-vs-Test">Action Words `Create` vs. `Test`</h1>

The document specifies the order of deploying resources for Flow-2. Generally, resources are created first, followed by their configuration and testing. However, some resources might be reused from previous flows, indicated by `Use`.

**Example:**

- **Kubernetes Cluster** needs to be created before testing it.
- **Cognito User Pool** requires creation and testing before other resources can interact with it.
- **S3 Bucket** follows the same creation and testing order.

<h1 id="Infrastructure-Resource-Unique-Identification">Infrastructure Resource Unique Identification</h1>

Infrastructure resources within the Sambar/LeBar/k8or web applications follow a standardized naming convention for identification. For example, `flow-2-inf-5` consists of:

* **flow-2:** Indicates the specific `User Registration` Flow-2 within the Sambar web application.
* **inf:** Denotes the resource type as an infrastructure component.
* **5:** Represents the sequence of the resource within the flow.

Each resource has a unique identifier that reflects its purpose and placement within the Sambar/LeBar/k8or applications. It's critical to adhere to this naming convention and maintain the established order of resource creation to ensure consistent and efficient operation of the web applications.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Application Resource Breakdown within the Sambar/LeBar/k8or Web Applications |
| | Description | This document uses `User Registration` Flow-2 as an example to illustrate the infrastructure resource breakdown. The same principles and processes apply to all other flows within the Sambar/LeBar/k8or web applications. |
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
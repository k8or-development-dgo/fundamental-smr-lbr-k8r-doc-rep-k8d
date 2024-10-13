## Sambar/LeBar/k8or Web Application Infrastructure Resource Breakdown

This document uses `User Registration` Flow-2 as an example to illustrate the infrastructure resource breakdown. The same principles and processes apply to all other flows within the Sambar/LeBar/k8or web applications.

## Content

1. **[Infrastructure Resource Types](#Infrastructure-Resource-Types)**
    * **[Kubernetes Cluster](#Kubernetes-Cluster)**
    * **[Kubernetes Namespaces](#Kubernetes-Namespaces)**
    * **[Kubernetes Secrets](#Kubernetes-Secrets)**
    * **[Ingress Resources](#Ingress-Resources)**
    * **[AWS Cognito](#AWS-Cognito)**
    * **[Database Clusters](#Database-Clusters)**
    * **[Cloud Storage](#Cloud-Storage)**
    * **[AWS Identity and Access Management `IAM`](#AWS-Identity-and-Access-Management-IAM)**
    * **[DigitalOcean Spaces Access Keys](#DigitalOcean-Spaces-Access-Keys)**
2. **[Action Words](#Action-Words)**
3. **[Infrastructure Creation Order](#Infrastructure-Creation-Order)**
4. **[Action Words `Create` vs. `Test`](#Action-Words-Create-vs-Test)**
5. **[Infrastructure Resource Unique Identification](#Infrastructure-Resource-Unique-Identification)**
6. **[Document Metadata](#Document-Metadata)**

<h1 id="Infrastructure-Resource-Types">Infrastructure Resource Types</h1>

Infrastructure repositories within the Sambar/LeBar/k8or web applications contain the following types of resources:

<h2 id="Kubernetes-Cluster">Kubernetes Cluster</h2>

* **Purpose:** The Kubernetes cluster serves as the foundational platform for orchestrating and managing microservices within the Sambar/LeBar/k8or web applications. It provides a robust and scalable environment for deploying, scaling, and managing the various microservices that compose these applications. The cluster ensures that the microservices are distributed efficiently across the available infrastructure, handles load balancing, and provides fault tolerance mechanisms for high availability and resilience.
* **Learn More:** Visit the provided URL for a detailed explanation of Kubernetes cluster solutions within this infrastructure:
    * **[Kubernetes Cluster Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir/kubernetes-cluster-dir)**
* **Understanding:** 
    * Kubernetes manages containerized deployments, allowing for efficient packaging and execution of microservices.
    * It automates scaling based on application needs, ensuring optimal resource utilization.
    * The cluster facilitates self-healing capabilities, automatically restarting failed containers or pods for high availability.
    * By offering a standardized platform, Kubernetes simplifies the development, deployment, and management of microservices across different environments.

<h2 id="Kubernetes-Namespaces">Kubernetes Namespaces</h2>

* **Purpose:** Create logical isolation units within the Kubernetes cluster. Namespaces enable separation of resources and workloads for different applications or environments.
* **Learn More:** Visit the provided URL for an in-depth explanation of Kubernetes namespaces and their benefits for managing resources within the Sambar/LeBar/k8or deployments:
    * **[Kubernetes Namespaces Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir/kubernetes-cluster-dir)** 
* **Understanding:** Explore how namespaces organize resources, enhance security, and support multi-tenancy within the Kubernetes cluster.

<h2 id="Kubernetes-Secrets">Kubernetes Secrets</h2>

* **Purpose:** Store sensitive information used by applications and services within the Kubernetes cluster. This includes DockerHub credentials and SSL certificates.
* **Learn More:** Visit the provided URL for detailed information on managing secrets securely within the Kubernetes environment used for Sambar/LeBar/k8or applications:
    * **[Kubernetes Secrets Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir/kubernetes-secrets-dir)** 
* **Understanding:** Explore how secrets are created, accessed securely by authorized services, and contribute to secure application deployments.

<h2 id="Ingress-Resources">Ingress Resources</h2>

* **Purpose:** Route external traffic from the internet to specific microservices deployed within the Kubernetes cluster. Ingress acts as a single entry point.
* **Learn More:** Visit the provided URL for a thorough explanation of Ingress resources and their configuration for routing traffic to the Sambar/LeBar/k8or web applications:
    * **[Ingress Resources Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir/ingress-resources-dir)** 
* **Understanding:** Explore how Ingress is configured, manages traffic flow, and directs external requests to the appropriate microservices within the cluster.

<h2 id="AWS-Cognito">AWS Cognito</h2>

* **Purpose:** Manages user identities and authentication for the Sambar/LeBar/k8or web applications. Cognito provides a user pool for secure login and access control.
* **Learn More:** Visit the provided URL for a comprehensive overview of AWS Cognito functionalities and its role in user management for these applications:
    * **[AWS Cognito Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir/aws-cognito-dir)** 
* **Understanding:** Explore how Cognito handles user registration, login, authentication workflows, and integrates with the applications for secure access.

<h2 id="Database-Clusters">Database Clusters</h2>

* **Purpose:** Stores application data required for the Sambar/LeBar/k8or web applications. These clusters can be MySQL or MongoDB deployments.
* **Learn More:** Visit the provided URL for specific information on managing database clusters used by these applications:
    * **[Database Clusters Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir/database-cluster-dir)** 
* **Understanding:** Explore how database clusters are configured, scaled, and secured to ensure optimal performance and data integrity for the applications.

<h2 id="Cloud-Storage">Cloud Storage</h2>

* **Purpose:** Stores data, logs, and images used by the Sambar/LeBar/k8or web applications. Examples include Amazon S3 or DigitalOcean Spaces.
* **Learn More:** Visit the provided URL for a detailed explanation of cloud storage solutions within this infrastructure:
    * **[Cloud Storage Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir/cloud-storage-dir)**
* **Understanding:** Explore how cloud storage integrates with the applications, its role in data persistence, and considerations for choosing a specific provider.

<h2 id="AWS-Identity-and-Access-Management-IAM">AWS Identity and Access Management `IAM`</h2>

* **Purpose:** Manages permissions and credentials for services within the infrastructure. IAM includes users, policies, roles, and access keys. 
* **Learn More:** Visit the provided URL for a deep dive into AWS IAM concepts and configurations relevant to Sambar/LeBar/k8or applications.
    * **[AWS Identity and Access Management `IAM` Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir/aws-iam-dir)**
* **Understanding:** Explore how IAM controls access to resources, defines user roles within the system, and secures sensitive information.

<h2 id="DigitalOcean-Spaces-Access-Keys">DigitalOcean Spaces Access Keys</h2>

* **Purpose:** Credentials specifically used to access data stored in DigitalOcean Spaces within the infrastructure.
* **Learn More:** Visit the provided URL for details on managing DigitalOcean Spaces access keys and security practices:
    * **[DigitalOcean Spaces Access Keys Explanation](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir/space-access-key-dir)**
* **Understanding:** Explore how access keys are generated, stored securely, and used to interact with DigitalOcean Spaces for data storage and retrieval.

<h1 id="Action-Words">Action Words</h1>

* **Create:** Setting up the resource for the first time.
* **Configure:** Defining initial parameters and configurations.
* **Test:** Verifying the functionality and proper operation.
* **Use:** Reusing a resource created in a previous flow.

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
| Document Metadata | Title | Sambar/LeBar/k8or Web Application Infrastructure Resource Breakdown |
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

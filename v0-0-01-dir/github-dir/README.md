# GitHub Organization Structure for Sambar/LeBar/k8or

This document outlines the structure and purpose of GitHub organizations within the Sambar/LeBar/k8or ecosystem, highlighting their role in isolating environments and managing development activities across different cloud providers.

## Content

1. **[Purpose of GitHub Organizations](#Purpose-of-GitHub-Organizations)**
2. **[Organization Structure](#Organization-Structure)**
3. **[Environment Isolation](#Environment-Isolation)**
4. **[Cloud Provider Separation](#Cloud-Provider-Separation)**
5. **[Repository Structure and Naming Conventions within Sambar/LeBar/k8or](#Repository-Structure-and-Naming-Conventions-within-Sambar-LeBar-k8or)**
6. **[Private Repository Configuration](#Private-Repository-Configuration)**
7. **[Document Metadata](#Document-Metadata)**

<h1 id="Purpose-of-GitHub-Organizations">Purpose of GitHub Organizations</h1>

Within the Sambar/LeBar/k8or ecosystem, GitHub organizations are employed to isolate and manage specific environments for each web application. This separation ensures that development, testing, staging, and production activities occur in distinct and controlled environments, mitigating risks and facilitating efficient collaboration.

<h1 id="Organization-Structure">Organization Structure</h1>

1. **Web Application Organizations:**
   * **Sambar:**
     - `sambar-development-dgo`: For Sambar development activities on DigitalOcean.
     - `sambar-development-aws`: For Sambar development activities on AWS.
   * **LeBar:**
     - `lebar-development-dgo`: For LeBar development activities on DigitalOcean.
     - `lebar-development-aws`: For LeBar development activities on AWS.
   * **k8or:**
     - `k8or-development-dgo`: For k8or development activities on DigitalOcean.
     - `k8or-development-aws`: For k8or development activities on AWS.

2. **Additional Organizations:**
   * Sambar/LeBar/k8or have additional GitHub organizations for internal maintenance, security-related tasks, or other specific purposes.

<h1 id="Environment-Isolation">Environment Isolation</h1>

Each GitHub organization represents a distinct environment within the Sambar/LeBar/k8or ecosystem. This separation allows for independent development, testing, and deployment processes, minimizing the risk of unintended changes or conflicts between environments.

<h1 id="Cloud-Provider-Separation">Cloud Provider Separation</h1>

The organizations are further divided based on the cloud provider used for deployment. This separation ensures that resources, configurations, and dependencies specific to each cloud provider are managed within their respective organizations, promoting flexibility and scalability.

<h1 id="Repository-Structure-and-Naming-Conventions-within-Sambar-LeBar-k8or">Repository Structure and Naming Conventions within Sambar/LeBar/k8or</h1>

**Repository Types**

Within each cloud provider-based GitHub organization, four primary repository types are maintained:

1. **[Infrastructure Repository](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/infrastructure-repository-dir):** Contains resources necessary for creating and configuring the underlying infrastructure components of a specific flow within the Sambar/Lebar/k8or web applications. This includes cloud services, Kubernetes clusters, namespaces, and other supporting elements.
2. **[Application Repository](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/application-repository-dir):** Houses the microservice code, configuration files and backend resources, such as MySQL tables, MongoDB collections, and PostgreSQL tables, specific to the application logic and functionality of a particular flow. This encompasses frontend and backend microservices and related backend resources.
3. **[Data Repository](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/data-repository-dir):** Stores the metadata and data required to prepare for the Sambar web application.
4. **[Population Repository](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/github-dir/population-repository-dir):** Contains documentation outlining the steps to load the prepared data into the backend resources of the Sambar web application.

### Explore and analyze the various repository types within the Sambar/LeBar/k8or GitHub organizations, including infrastructure, application, data, and population repositories. This analysis should involve opening dedicated URLs for each repository type to gain a deeper understanding of their contents and purpose.

### To effectively study and work within the Sambar/LeBar/k8or web applications, it's essential to follow a consistent order: always begin by exploring infrastructure repositories (1), then proceed to application repositories (2), followed by data repositories (3), and finally population repositories (4) within each flow.

**Naming Convention**

The naming convention for these repositories follows a consistent structure:

```
flow-[flow_number]-[repository_type]-rep-sd2-dgo
```

**Components:**

* **`flow-[flow_number]`:** Identifies the specific flow to which the repository belongs.
* **`[repository_type]`:** Specifies the type of repository, such as infrastructure, application, data, or population.
* **`rep`:** A classifier indicating a repository.
* **`sd2`:** Indicates the operational environment. `sd2` signifies the Sambar web application development environment. The suffix `2` was added to differentiate this environment from the original development environment `sd` after it was migrated to a different AWS region and account. This distinction helps prevent resource conflicts and confusion across regions.
* **`dgo`:** Represents the cloud provider, DigitalOcean in this case.

**Example:**

`flow-1-infrastructure-rep-sd2-dgo`

* **`flow-1`:** Indicates the first flow within the Sambar web application.
* **`infrastructure`:** Specifies that this is an infrastructure repository.
* **`rep`:** Classifier indicating a repository.
* **`sd2`:** Indicates the operational environment. `sd2` signifies the Sambar web application development environment. The suffix `2` was added to differentiate this environment from the original development environment `sd` after it was migrated to a different AWS region and account. This distinction helps prevent resource conflicts and confusion across regions.
* **`dgo`:** Represents DigitalOcean as the cloud provider.


<h1 id="Private-Repository-Configuration">Private Repository Configuration</h1>

All GitHub organizations within the Sambar/LeBar/k8or ecosystem should be configured as private to safeguard the confidentiality and security of the codebase and related resources. This prevents unauthorized access to repositories and protects intellectual property.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | GitHub Organization Structure for Sambar/LeBar/k8or |
| | Description | This document outlines the structure and purpose of GitHub organizations within the Sambar/LeBar/k8or ecosystem, highlighting their role in isolating environments and managing development activities across different cloud providers. |
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
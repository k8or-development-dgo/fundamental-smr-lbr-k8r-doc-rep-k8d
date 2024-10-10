## DockerHub Organization Structure for Sambar/LeBar/k8or

This document delineates the structure and rationale behind the DockerHub organizations employed within the Sambar/LeBar/k8or ecosystem. These organizations play a critical role in isolating and managing distinct environments for each web application, thereby mitigating risks and fostering efficient collaboration.

## Content

1. **[Purpose of GitHub Organizations](#Purpose-of-GitHub-Organizations)**
2. **[Organization Structure](#Organization-Structure)**
3. **[Environment Isolation](#Environment-Isolation)**
4. **[Naming Convention](#Naming-Convention)**
5. **[Document Metadata](#Document-Metadata)**

<h1 id="Purpose-of-DockerHub-Organizations">Purpose of DockerHub Organizations</h1>

Within the Sambar/LeBar/k8or ecosystem, DockerHub organizations are employed to isolate and manage specific environments for each web application. This separation ensures that development, testing, staging, and production activities occur in distinct and controlled environments, mitigating risks and facilitating efficient collaboration.

<h1 id="Organization-Structure">Organization Structure</h1>

1. **Sambar:**
   * `sambardev`: Dedicated to housing Docker images of Sambar development microservices, regardless of the underlying cloud provider.
2. **Lebar:**
   * `lebardev`: Designed to store Docker images of LeBar development microservices, irrespective of the cloud provider.
3. **K8or:**
   * `k8ordev`: Houses Docker images of k8or development microservices, adaptable to various cloud environments.

<h1 id="Environment-Isolation">Environment Isolation</h1>

Each DockerHub organization serves as an isolated environment within the Sambar/LeBar/k8or ecosystem. This separation empowers independent development, testing, and deployment processes, minimizing the likelihood of unintended changes or conflicts between environments.

<h1 id="Naming-Convention">Naming Convention</h1>

The naming convention for these organizations follows a consistent pattern:

* **[web_application_name]dev:**
  * `[web_application_name]`: Represents the name of the web application, such as Sambar, LeBar, or k8or.
  * `dev`: Three-letter code indicates the development environment.

For example, `sambardev` signifies the DockerHub organization for storing Sambar development microservice images.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | DockerHub Organization Structure for Sambar/LeBar/k8or |
| | Description | This document delineates the structure and rationale behind the DockerHub organizations employed within the Sambar/LeBar/k8or ecosystem. These organizations play a critical role in isolating and managing distinct environments for each web application, thereby mitigating risks and fostering efficient collaboration. |
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
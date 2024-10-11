# Resource Naming Conventions in the Sambar/LeBar/k8or Web Applications

This document outlines the naming conventions used for various technical resources within the Sambar/LeBar/k8or web applications. Consistent and descriptive naming practices enhance code readability, maintainability, and facilitate efficient resource management.

## Content

1. **[Resource Technical Name](#Resource-Technical-Name)**
2. **[Microservice Naming Convention](#Microservice-Naming-Convention)**
3. **[Middle Resource Naming Convention](#Middle-Resource-Naming-Convention)**
4. **[Backend Resource Naming Convention](#Backend-Resource-Naming-Convention)**
5. **[Document Metadata](#Document-Metadata)**

<h1 id="Resource-Technical-Name">Resource Technical Name</h1>

- **Purpose:** Used for internal, system-oriented identification.
- **Characteristics:**
  - Must be unique within the system or environment to avoid naming conflicts.
  - Not intended to be user-friendly or easily memorable.
  - May include long alphanumeric strings or specific classifiers that are meaningful to the system but not necessarily to end-users.

<h1 id="Microservice-Naming-Convention">Microservice Naming Convention</h1>

- **Structure:** `<Microservice Identifier>-<Subscription Plan>-<Country>-<Language>-<Environment>-<Region>`
- **Example 1: Sambar Microservice**
    - `ub0209-no-us-en-sd2-lo`
    - Breakdown:
        - `ub0209`: Microservice Identifier ("ub" for "user-board", "02" for Flow 2, "09" for Block 9)
        - `no`: No subscription plan
        - `us`: USA (country)
        - `en`: English (language)
        - `sd2`: Sambar development environment (see note below)
        - `lo`: London (AWS region)
- **Example 2: LeBar Microservice**
    - `ua0306-no-us-en-ld-lo`
    - Breakdown:
        - `ua0306`: Microservice Identifier ("ua" for "User-Authentication", "03" for Flow 3, "06" for Block 6)
        - `no`: No subscription plan
        - `us`: USA (country)
        - `en`: English (language)
        - `ld`: LeBar development environment (see note below)
        - `lo`: London (AWS region)
- **Microservice Identifier:**
    - **Alphabetic prefix:** Initial letters of the microservice's full name
    - **Numeric suffix:** Flow and BLOCK where the microservice is defined
- **Environment IDs:**
    - Sambar: 
        - Two-character code starting with 's', followed by:
            - `d`: development
            - `t`: testing
            - `p`: production
            - `s`: staging
    - LeBar: 
        - Two-character code starting with 'l', followed by:
            - `d`: development
            - `t`: testing
            - `p`: production
            - `s`: staging
    - k8or: 
        - Two-character code starting with 'k', followed by:
            - `d`: development
            - `t`: testing
            - `p`: production
            - `s`: staging
  - **Exception:** `sd2` is used in the examples as a specific exception for a second Sambar development environment. Generally, avoid using numerical digits within environment identifiers.

<h1 id="Middle-Resource-Naming-Convention">Middle Resource Naming Convention</h1>

- **Types:**
    - Between frontend and backend microservices
    - Between backend microservices and databases
    - Dedicated to MySQL database creation
- **Example 1: Frontend-Backend Communication**
    - `ub0209-no-us-en-sd2-lo-ua0203-no-us-en-sd2-lo-policy-sd2`
    - Breakdown:
        - `ub0209-no-us-en-sd2-lo`: Frontend microservice
        - `ua0203-no-us-en-sd2-lo`: Backend microservice
        - `policy`: IAM Policy (type of middle resource)
        - `sd2`: Sambar development environment
- **Example 2: Backend-Database Communication**
    - `ua0203-no-us-en-sd2-lo-user-registration-image-03203-w-role-sd2`
    - Breakdown:
        - `ua0203-no-us-en-sd2-lo`: Backend microservice
        - `user-registration-image-03203`: Backend resource identifier (S3 Bucket in this case)
        - `w`: Write operation (could also be 'r' for read)
        - `role`: IAM Role (type of middle resource)
        - `sd2`: Sambar development environment
- **Example 3: MySQL Database Creation**
    - `user-account-number-0203-subnet-group-sd2`
    - Breakdown:
        - `user-account-number-0203`: Backend resource identifier (MySQL database)
        - `subnet-group`: Subnet Group (type of middle resource)
        - `sd2`: Sambar development environment

<h1 id="Backend-Resource-Naming-Convention">Backend Resource Naming Convention</h1>

- **Structure:** `<Backend Resource Function Identifier> + <Flow and Block Number> + <Environment>`
- **Example 1:**
    - `user-invitation-code-0209-sd2`
    - Breakdown:
        - `user-invitation-code`: Backend resource function identifier
        - `0209`: Flow 2, Block 9
        - `sd2`: Sambar development environment
- **Example 2:**
    - `user-session-02403-sd2`
    - Breakdown:
        - `user-session`: Backend resource function identifier
        - `02403`: Flow 024 (designated for DynamoDB), Block 3
        - `sd2`: Sambar development environment

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Resource Naming Conventions in the Sambar/LeBar/k8or Web Applications |
| | Description | This document outlines the naming conventions used for various technical resources within the Sambar/LeBar/k8or web applications. Consistent and descriptive naming practices enhance code readability, maintainability, and facilitate efficient resource management. |
| | Identification | TBD | |
| | Version | v0-0-01 | |
| | Format | md | |
| | Revision | This is the first version uploaded to the ChatBOT. |
| | Author | Anna/Barb.Rock |
| | Date | October 11, 2024 |
| Subject Metadata | Alias | TBD |
| |  Name | TBD |
| |  FQID | TBD |
| |  Version | s0-0-01 |
| |  Action | 000010 |
| hGraph Metadata | Alias | none |
| |  Name | none |
| |  FQID | none |
| |  Version | none |
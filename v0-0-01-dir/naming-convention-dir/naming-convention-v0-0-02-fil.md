## **Resource Naming Conventions in the Sambar/LeBar Web Application**

This document outlines the naming conventions used for various technical resources within the Sambar and LeBar web applications. Consistent and descriptive naming practices enhance code readability, maintainability, and facilitate efficient resource management within the AWS (Amazon Web Services) ecosystem.

## Resource Technical Name

- **Purpose:** Used for internal, system-oriented identification.
- Characteristics:
  - Must be unique within the system or environment to avoid naming conflicts.
  - Not intended to be user-friendly or easily memorable.
  - May include long alphanumeric strings or specific classifiers that are meaningful to the system but not necessarily to end-users.

## Naming Conventions

### Microservices

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

- **Note on Environment IDs:**

  - Sambar:

     Two-character code starting with 's', followed by:

    - `d`: development
    - `t`: testing
    - `p`: production
    - `s`: staging

  - **LeBar:** Two-character code starting with 'l', followed by the same single-letter designations as Sambar.

  - **Exception:** `sd2` is used in the examples as a specific exception for a second Sambar development environment. Generally, avoid using numerical digits within environment identifiers.

### Middle Resources

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

### Backend Resources

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

**Remember:**

- Microservice Identifier:
  - Alphabetic prefix: Initial letters of the microservice's full name
  - Numeric suffix: Flow and BLOCK where the microservice is defined

This revised document, formatted for a GitHub repo, provides a clear and comprehensive overview of the naming conventions used in the Sambar and LeBar web applications. It includes explanations for each component of the naming structures and highlights the importance of consistent naming practices for effective resource management and development.
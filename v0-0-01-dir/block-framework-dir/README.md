## BLOCK Framework witin the Sambar/LeBar/k8or Web Applications

The BLOCK framework offers a modular and efficient approach to constructing web and mobile application backends. This breakdown delves deeper into each component and explores how they work together to achieve functionality.

## Content

1. **[Flows: The Functional Backbones](#Flows-The-Functional-Backbones)**
2. **[Traditional Sambar Flows](#Traditional-Sambar-Flows)**
3. **[Integrated Sambar Flows](#Integrated-Sambar-Flows)**
4. **[Traditional LeBar Flows](#Traditional-LeBar-Flows)**
5. **[Integrated LeBar Flows](#Integrated-LeBar-Flows)**
6. **[Traditional k8or Flows](#Traditional-k8or-Flows)**
7. **[BLOCKs: The Workhorse Components](#BLOCKs-The-Workhorse-Components)**
8. **[Legs: Microscopic Execution Units](#Legs-Microscopic-Execution-Units)**
9. **[Assets and Resources: Powering the Legs](#Assets-and-Resources-Powering-the-Legs)**
10. **[The BLOCK Framework in Action: A Collaborative Dance](#The-BLOCK-Framework-in-Action-A-Collaborative-Dance)**
11. **[Benefits of the BLOCK Framework](#Benefits-of-the-BLOCK-Framework)**
12. **[Additional Benefits](#Additional-Benefits)**
13. **[Document Metadata](#Document-Metadata)**

<h1 id="Flows-The-Functional-Backbones">Flows: The Functional Backbones</h1>

Imagine a Flow as the core of a specific functionality within the Sambar/LeBar/k8or web applications. It represents a well-defined sequence of operations and processes that data and requests follow to achieve a particular goal. Examples include `User Registration` or `Product Purchase`. These Flows act as blueprints for the Sambar/LeBar/k8or web application's functionalities, outlining the steps required to deliver desired outcomes.

<h1 id="Traditional-Sambar-Flows">Traditional Sambar Flows</h1>

These flows represent core functionalities within the Sambar web application.

* **Flow-1** `Site Static Page` hosted on [sambar.one](https://www.sambar.one)
* **Flow-2** `User Registration`
* **Flow-3** `User Login`
* **Flow-4** `User Profile`
* **Flow-5** `User Subscription`
* **Flow-6** `User Add LeBar`
* **Flow-7** `User Profile Tab`
* **Flow-8** is available
* **Flow-9** `T-Input Form`
* **Flow-10** `Opportunity Board`
* **Flow-11** `Strategy Board`
* **Flow-12** `Trade Board`
* **Flow-13** `LeBar to Credit`
* **Flow-14** `Historical Dashboard`
* **Flow-15** `Real-Time`
* **Flow-16** `Group Trade Internal Process`
* **Flow-17** `Widget`
* **Flow-18** `Demo`
* **Flow-19** `Symbol`
* **Flow-20** is available
* **Flow-21** is available
* **Flow-22** is available
* **Flow-23** `Article Portal`
* **Flow-24** is available
* **Flow-25** `Group Trade Leader` 
* **Flow-26** `Group Trade Follower`
* **Flow-27** `Group Trade Widget`
* **Flow-51** `Analyst Registration`
* **Flow-52** `Analyst Login`
* **Flow-53** `Analyst Profile`
* **Flow-54** `Analyst Subscription`
* **Flow-55** `Analyst Add LeBar`
* **Flow-56** `Analyst Profile Tab`

<h1 id="Integrated-Sambar-Flows">Integrated Sambar Flows</h1>

These flows integrate functionalities between Sambar and LeBar's backend.

* **Flow-72** `Sambar-LeBar User Registration`

<h1 id="Traditional-LeBar-Flows">Traditional LeBar Flows</h1>

These flows represent core functionalities within the LeBar web application.

* **Flow-1** `Site Static Page` hosted on [lebar.digital](https://www.lebar.digital)
* **Flow-2** `User Registration`
* **Flow-3** `User Login`
* **Flow-4** `User Profile`
* **Flow-5** `User Subscription`
* **Flow-6** `Purchase LeBar`
* **Flow-7** `Cent to LeBar`
* **Flow-8** `User Profile tab`
* **Flow-9** `Transfer LeBar`
* **Flow-10** `Withdrawal LeBar`
* **Flow-11** `Move LeBar`

<h1 id="Integrated-LeBar-Flows">Integrated LeBar Flows</h1>

These flows integrate functionalities within the LeBar application. 

* **Flow-51** `User Registration`
* **Flow-52** `User Login`
* **Flow-53** `Purchase LeBar`
* **Flow-54** `Notification tab`
* **Flow-55** `Cent to LeBar`
* **Flow-56** `Move LeBar`
* **Flow-57** `Transfer LeBar`
* **Flow-58** `Withdrawal LeBar`

<h1 id="Traditional-k8or-Flows">Traditional k8or Flows</h1>

These flows represent core functionalities within the k8or web application.

* **Flow-1** `Site Static Page` hosted on [k8or.com](https://www.k8or.com)
* **Flow-41** `ChatBOT`
* **Flow-42** `jGraph` (`JSON Crack`)
* **Flow-43** `KSecret` (`PrivateBin`)
* **Flow-44** `Everest` (`Mattermost`)
* **Flow-45** `Autodo` (`n8n`)
* **Flow-46** `Portainer`
* **Flow-61** `empower99.win` hosted on [empower99.win](https://www.empower99.win)
* **Flow-62** `rajmarni.com` hosted on [rajmarni.com](https://www.rajmarni.com)

<h1 id="BLOCKs-The-Workhorse-Components">BLOCKs: The Workhorse Components</h1>

![Alt text](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/block-framework-dir/diagram-dir/f2b3-user-registration-sd2-v.0.1.26.pdf)

Within each Flow lie BLOCKs, the fundamental building blocks of the framework. These are interconnected components, each responsible for a specific task within the Flow. Consider a User Registration Flow – it might contain a BLOCK dedicated to collecting user data, another for validating it, and yet another for storing it securely. Each BLOCK focuses on a single step in the larger process, promoting modularity and clarity within the codebase.

<h1 id="Legs-Microscopic-Execution-Units">Legs: Microscopic Execution Units</h1>

![Alt text](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/block-framework-dir/diagram-dir/leg-example-v0-0-01-fil.png)

Zooming in further, we encounter Legs residing within each BLOCK. These are akin to microscopic veins carrying out specific functions within the BLOCK. For example, a BLOCK responsible for collecting user documents might have one Leg for collecting PDF files and another for uploading them to an S3 bucket. Each Leg handles a unique sub-task within the BLOCK, adding another layer of granularity and flexibility to the framework.

<h1 id="Assets-and-Resources-Powering-the-Legs">Assets and Resources: Powering the Legs</h1>

![Alt text](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/block-framework-dir/diagram-dir/asset-example-v0-0-01-fil.png)

Legs are where Assets and Resources come into play. Think of an Asset as the brain of a Leg – a microservice, API gateway, database, S3 bucket, or any entity with built-in intelligence or data persistence capabilities. In the S3 Leg example, the S3 bucket itself is the Asset. Resources, on the other hand, act as keys unlocking that intelligence or data. IAM Roles, Policies, and Secrets are all examples of Resources, granting access and permissions to the capabilities of the associated Asset.

<h1 id="The-BLOCK-Framework-in-Action-A-Collaborative-Dance">The BLOCK Framework in Action: A Collaborative Dance</h1>

Now, imagine how these components work together in a coordinated fashion:

1. **Flow Trigger:** A user initiates an action, triggering the User Registration Flow.
2. **Flow Orchestration:** The Flow directs data and requests through interconnected BLOCKs, ensuring they are processed in the correct sequence.
3. **BLOCK Execution:** Within each BLOCK, Legs handle specific tasks like collecting documents, validating data, or uploading files.
4. **Leveraging Assets:** Each Leg utilizes its designated Asset (e.g., S3 bucket) for intelligent processing or data storage.
5. **Resource Management:** Resources (e.g., IAM Roles) ensure secure access and proper functioning of the Assets.

<h1 id="Benefits-of-the-BLOCK-Framework">Benefits of the BLOCK Framework</h1>

This modular framework offers several advantages for developers:

* **Scalability:** Adding new features or scaling existing ones becomes easier. New BLOCKs and Legs can be introduced or modified without impacting the entire Flow.
* **Maintainability:** Debugging and updating specific functionalities are simplified by pinpointing issues within individual BLOCKs.
* **Reusability:** Common BLOCKs can be reused across different Flows, saving development time and effort.
* **Transparency:** The defined structure provides clarity for developers working on the codebase, making it easier to understand and maintain.
* **Visualization:** To further enhance understanding, consider creating visual aids like diagrams or flowcharts. These can depict the relationships between Flows, BLOCKs, Legs, Assets, and Resources, making the framework even more transparent and comprehensible.

<h1 id="Additional-Benefits">Additional Benefits</h1>

* **Flexibility:** The BLOCK framework's modular nature allows for easy customization and adaptation to different project requirements.
* **Efficiency:** By breaking down complex functionalities into smaller, manageable units, the BLOCK framework can improve development efficiency and reduce the risk of errors.
* **Collaboration:** The framework promotes collaboration among team members by clearly defining roles and responsibilities within each Flow.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | BLOCK Framework witin the Sambar/LeBar/k8or Web Applications |
| | Description | The BLOCK framework offers a modular and efficient approach to constructing web and mobile application backends. This breakdown delves deeper into each component and explores how they work together to achieve functionality. |
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
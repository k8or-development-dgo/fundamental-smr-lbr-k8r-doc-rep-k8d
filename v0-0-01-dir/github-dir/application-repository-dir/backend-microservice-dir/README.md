# Application Backend Microservice Breakdown within the Sambar/LeBar/k8or Web Applications

This document provides a comprehensive overview of the backend microservice application resources utilized within the Sambar/LeBar/k8or web applications. It outlines the types of repositories involved, the naming conventions employed, and the various microservice types that contribute to the application's functionality.

## Content

1. **[Microservice Application Repository Types](#Microservice-Application-Repository-Types)**
2. **[Naming Convention for Microservice Application Repositories](#Naming-Convention-for-Microservice-Application-Repositories)**
3. **[Sambar Microservice Types](#Sambar-Microservice-Types)**
    * **[Sambar User Management and Authentication Microservices](#Sambar-User-Management-and-Authentication-Microservices)**
    * **[Sambar Subscription and Payment Microservices](#Sambar-Subscription-and-Payment-Microservices)**
    * **[Sambar Trade Execution and Management Microservices](#Sambar-Trade-Execution-and-Management-Microservices)**
    * **[Sambar Data Processing and Analytics Microservices](#Sambar-Data-Processing-and-Analytics-Microservices)**
    * **[Sambar Frontend and UI Microservices](#Sambar-Frontend-and-UI-Microservices)**
    * **[Sambar Data and Content Management Microservices](#Sambar-Data-and-Content-Management-Microservices)**
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

<h1 id="Sambar-Microservice-Types">Sambar Microservice Types</h1>

The Sambar/LeBar/k8or web application utilizes a diverse range of microservices to implement various functionalities. 

<h2 id="Sambar-User-Management-and-Authentication-Microservices">Sambar User Management and Authentication Microservices</h2>

| Microservice Name | Abbreviation | Description |
|---|---|---|
| User Authentication | `ua` | Handles user authentication and authorization. |
| User Invitation | `ui` | Manages user invitations. |
| User SMS Notification | `usn` | Sends SMS notifications to users. |
| User Information Payload | `uip` | Stores and manages user information. |
| User Payload Event Log | `upel` | Logs user payload events. |
| Authorization | `auth` | Handles authorization for different actions. |
| Analyst Authentication | `aa` | Handles analyst authentication and authorization. |
| Analyst Invitation | `ai` | Manages analyst invitations. |
| Analyst SMS Notification | `asn` | Sends SMS notifications to analysts. |

<h2 id="Sambar-Subscription-and-Payment-Microservices">Sambar Subscription and Payment Microservices</h2>

| Microservice Name | Abbreviation | Description |
|---|---|---|
| Subscription | `sub` | Manages user subscriptions. |
| Credit Total | `ct` | Calculates and manages user credit totals. |
| LeBar Total | `lt` | Calculates and manages LeBar totals. |
| LeBar Cent Information | `lci` | Provides information about LeBar cents. |
| Add LeBar | `al` | Adds LeBar to user accounts. |
| Move LeBar | `ml` | Moves LeBar between different accounts or purposes. |
| Cent to LeBar | `ctl` | Converts cents to LeBar. |
| Credit Distribution | `cd` | Distributes credit among users. |
| Convert Credit Event Log | `ccel` | Logs credit conversion events. |
| User Board Notification | `ubn` | Handles user board notifications. |

<h2 id="Sambar-Trade-Execution-and-Management-Microservices">Sambar Trade Execution and Management Microservices</h2>

| Microservice Name | Abbreviation | Description |
|---|---|---|
| Trade Order | `to` | Manages trade orders. |
| T-Input Logic | `tl` | Handles T-Input logic for trades. |
| Strategy Search Data | `ssd` | Stores and manages strategy search data. |
| Strategy Subscription Event Log | `ssel` | Logs strategy subscription events. |
| Trade Data | `td` | Stores and manages trade data. |
| Group Trade Logic | `gtl` | Handles group trade logic. |
| Group Trade Widget Logic | `gtwl` | Provides widget logic for group trades. |
| Group Trade Transaction ID | `gtti` | Manages group trade transaction IDs. |
| Group Trade Unwind | `gtuw` | Unwinds group trades. |
| Group Trade Profit | `gtp` | Calculates group trade profits. |
| Group Trade Fee Penalty | `gtfp` | Calculates group trade fee penalties. |
| Group Trade Loss | `gtls` | Calculates group trade losses. |
| Group Trade Wind | `gtw` | Manages group trade wind. |
| Unwind Profit Loss Distribution Backend | `uwpld` | Handles unwind profit loss distribution. |
| Demo Trade Equity Outright | `deo` | Provides a demo for equity outright trades. |
| Demo Trade Equity Two Leg Spread | `detls` | Provides a demo for equity two leg spread trades. |
| Demo Trade Future Outright | `dfo` | Provides a demo for future outright trades. |
| Demo Trade Future Two Leg Spread | `dftls` | Provides a demo for future two leg spread trades. |
| Demo Trade Future ETF Spread | `dfetfs` | Provides a demo for future ETF spread trades. |
| Demo Trade Future ETN Spread | `dfetns` | Provides a demo for future ETN spread trades. |

<h2 id="Sambar-Data-Processing-and-Analytics-Microservices">Sambar Data Processing and Analytics Microservices</h2>

| Microservice Name | Abbreviation | Description |
|---|---|---|
| Trade Data Verify | `tdv` | Verifies trade data. |
| Historic Average | `ha` | Calculates historic averages. |
| Strategy Statistic | `ss` | Calculates strategy statistics. |
| Historic Future Data | `hfd` | Stores and manages historic future data. |
| Formula Historic Future Outright | `fm-hfo` | Calculates historic future outright values. |
| Formula Historic Future Two Leg Spread | `fm-hftls` | Calculates historic future two leg spread values. |
| Formula Historic Future Equity Spread | `fm-hfes` | Calculates historic future equity spread values. |
| Real-Time Provider | `rtp` | Provides real-time data. |
| Real-Time Process | `rtprc` | Processes real-time data. |
| Real-Time Nodejs | `rtn` | Handles real-time processing using Node.js. |
| Formula Group Trade Equity Outright | `fm-geo` | Calculates group trade equity outright values. |
| Formula Group Trade Two Leg Spread | `fm-getls` | Calculates group trade two leg spread values. |
| Formula Group Trade Future Outright | `fm-gfo` | Calculates group trade future outright values. |
| Formula Group Trade Future Two Leg Spread | `fm-gftls` | Calculates group trade future two leg spread values. |
| Formula Group Trade Future Equity Spread | `fm-gfes` | Calculates group trade future equity spread values. |
| Historic Chart | `hc` | Generates historic charts. |
| Analyst Strategy Information | `asi` | Provides information about analyst strategies. |
| Formula Historic Equity Outright | `fm-heo` | Calculates historic equity outright values. |
| Historic Equity Data | `hed` | Stores and manages historic equity data. |
| Formula Historic Equity Two Leg Spread | `fm-hetls` | Calculates historic equity two leg spread values. |
| Formula Widget Equity Outright | `fm-weo` | Calculates widget equity outright values. |
| Formula Widget Equity Two Leg Spread | `fm-wetls` | Calculates widget equity two leg spread values. |
| Formula Widget Future Two Leg Spread | `fm-wftls` | Calculates widget future two leg spread values. |
| Formula Widget Future Equity Spread | `fm-wfes` | Calculates widget future equity spread values. |
| Formula Symbol Equity Spread | `fm-ses` | Calculates formula symbol equity spread. |

<h2 id="Sambar-Frontend-and-UI-Microservices">Sambar Frontend and UI Microservices</h2>

| Microservice Name | Abbreviation | Description |
|---|---|---|
| Site Static Page | `ssp` | Handles static pages of the website. |
| User Board | `ub` | Provides the user board interface. |
| Add LeBar Form | `alf` | Provides the form for adding LeBar. |
| T-Input UI | `tu` | Provides the T-Input user interface. |
| Widget Equity Two Leg Spread | `wetls` | Provides the widget for equity two leg spread. |
| Widget Future Outright Seasonal | `wfos` | Provides the widget for future outright seasonal data. |
| Widget Future Two Leg Spread | `wftls` | Provides the widget for future two leg spread. |
| Widget Future Stock Spread | `wfss` | Provides the widget for future stock spread. |
| Widget Natural Gas Term | `wngt` | Provides the widget for natural gas term. |
| Widget Gasoline RB Term | `wgrbt` | Provides the widget for gasoline RB term. |
| Widget Heating Oil Term | `whot` | Provides the widget for heating oil term. |
| Widget Brent Crude Oil Term | `wbcot` | Provides the widget for Brent Crude Oil term. |
| Widget WTI Crude Oil Term | `wwticot` | Provides the widget for WTI Crude Oil term. |
| Widget Symbol Overview | `wso` | Provides an overview of symbols. |
| Widget Symbol History Overview | `wsho` | Provides an overview of symbol history. |
| Article Portal Board | `apb` | Provides the article portal board. |
| Article Portal | `ap` | Handles article portal functionality. |
| Analyst Board | `ab` | Provides the analyst board interface. |
| Symbol | `sym` | Manages symbols. |
| Widget Ticker | `wt` | Provides the widget ticker. |

<h2 id="Sambar-Data-and-Content-Management-Microservices">Sambar Data and Content Management Microservices</h2>

| Microservice Name | Abbreviation | Description |
|---|---|---|
| Analyst Article CMS | `aac` | Manages analyst articles. |

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
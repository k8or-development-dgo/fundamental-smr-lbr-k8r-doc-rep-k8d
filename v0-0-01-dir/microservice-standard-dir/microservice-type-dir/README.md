# Microservice Catalog for the Sambar/LeBar/k8or Web Applications

This document serves as a comprehensive catalog of all frontend and backend microservices deployed within the Sambar/LeBar/k8or web applications. It provides a centralized repository of information about each microservice.

## Content

1. **[Sambar Microservice Types](#Sambar-Microservice-Types)**
    * **[Sambar User Management and Authentication Microservices](#Sambar-User-Management-and-Authentication-Microservices)**
    * **[Sambar Subscription and Payment Microservices](#Sambar-Subscription-and-Payment-Microservices)**
    * **[Sambar Trade Execution and Management Microservices](#Sambar-Trade-Execution-and-Management-Microservices)**
    * **[Sambar Data Processing and Analytics Microservices](#Sambar-Data-Processing-and-Analytics-Microservices)**
    * **[Sambar Frontend and UI Microservices](#Sambar-Frontend-and-UI-Microservices)**
    * **[Sambar Data and Content Management Microservices](#Sambar-Data-and-Content-Management-Microservices)**
2. **[Document Metadata](#Document-Metadata)**

<h1 id="Sambar-Microservice-Types">Sambar Microservice Types</h1>

The Sambar microservice catalog specifically focuses on the microservices that are integral to the Sambar web application. It includes microservices responsible for tasks such as user authentication, data management, business logic, and API interactions within the Sambar ecosystem.

<h2 id="Sambar-User-Management-and-Authentication-Microservices">Sambar User Management and Authentication Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| **User Authentication** Backend Microservice | `ua` | Handles user authentication and authorization. | |
| **User Invitation** Backend Microservice | `ui` | Manages user invitations. | |
| **User SMS Notification** Backend Microservice | `usn` | Sends SMS notifications to users. | |
| **User Information Payload** Backend Microservice | `uip` | Stores and manages user information. | |
| **User Payload Event Log** Backend Microservice | `upel` | Logs user payload events. | |
| **Authorization** Backend Microservice | `auth` | Handles authorization for different actions. | |
| **Analyst Authentication** Backend Microservice | `aa` | Handles analyst authentication and authorization. | |
| **Analyst Invitation** Backend Microservice | `ai` | Manages analyst invitations. | |
| **Analyst SMS Notification** Backend Microservice | `asn` | Sends SMS notifications to analysts. | |

<h2 id="Sambar-Subscription-and-Payment-Microservices">Sambar Subscription and Payment Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| **Subscription** Backend Microservice | `sub` | Manages user subscriptions. | |
| **Credit Total** Backend Microservice | `ct` | Calculates and manages user credit totals. | |
| **LeBar Total** Backend Microservice | `lt` | Calculates and manages LeBar totals. | |
| **LeBar Cent Information** Backend Microservice | `lci` | Provides information about LeBar cents. | |
| **Add LeBar** Backend Microservice | `al` | Adds LeBar to user accounts. | |
| **Move LeBar** Backend Microservice | `ml` | Moves LeBar between different accounts or purposes. | |
| **Cent to LeBar** Backend Microservice | `ctl` | Converts cents to LeBar. | |
| **Credit Distribution** Backend Microservice | `cd` | Distributes credit among users. | |
| **Convert Credit Event Log** Backend Microservice | `ccel` | Logs credit conversion events. | |
| **User Board Notification** Backend Microservice | `ubn` | Handles user board notifications. | |

<h2 id="Sambar-Trade-Execution-and-Management-Microservices">Sambar Trade Execution and Management Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| **Trade Order** Backend Microservice | `to` | Manages trade orders. | |
| **T-Input Logic** Backend Microservice | `tl` | Handles T-Input logic for trades. | |
| **Strategy Search Data** Backend Microservice | `ssd` | Stores and manages strategy search data. | |
| **Strategy Subscription Event Log** Backend Microservice | `ssel` | Logs strategy subscription events. | |
| **Trade Data** Backend Microservice | `td` | Stores and manages trade data. | |
| **Group Trade Logic** Backend Microservice | `gtl` | Handles group trade logic. | |
| **Group Trade Widget Logic** Backend Microservice | `gtwl` | Provides widget logic for group trades. | |
| **Group Trade Transaction Identification** Backend Microservice | `gtti` | Manages group trade transaction IDs. | |
| **Group Trade Unwind** Backend Microservice | `gtuw` | Unwinds group trades. | |
| **Group Trade Profit** Backend Microservice | `gtp` | Calculates group trade profits. | |
| **Group Trade Fee Penalty** Backend Microservice | `gtfp` | Calculates group trade fee penalties. | |
| **Group Trade Loss** Backend Microservice | `gtls` | Calculates group trade losses. | |
| **Group Trade Wind** Backend Microservice | `gtw` | Manages group trade wind. | |
| **Unwind Profit Loss** Distribution Backend Microservice | `uwpld` | Handles unwind profit loss distribution. | |
| **Demo Trade Equity Outright** Backend Microservice | `deo` | Provides a demo for equity outright trades. | |
| **Demo Trade Equity Two Leg Spread** Backend Microservice | `detls` | Provides a demo for equity two leg spread trades. | |
| **Demo Trade Future Outright** Backend Microservice | `dfo` | Provides a demo for future outright trades. | |
| **Demo Trade Future Two Leg Spread** Backend Microservice | `dftls` | Provides a demo for future two leg spread trades. | |
| **Demo Trade Future ETF Spread** Backend Microservice | `dfetfs` | Provides a demo for future ETF spread trades. | |
| **Demo Trade Future ETN Spread** Backend Microservice | `dfetns` | Provides a demo for future ETN spread trades. | |

<h2 id="Sambar-Data-Processing-and-Analytics-Microservices">Sambar Data Processing and Analytics Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| **Trade Data Verify** Backend Microservice | `tdv` | Verifies trade data. | |
| **Historic Average** Backend Microservice | `ha` | Calculates historic averages. | |
| **Strategy Statistic** Backend Microservice | `ss` | Calculates strategy statistics. | |
| **Historic Future Data** Backend Microservice | `hfd` | Stores and manages historic future data. | |
| **Formula Historic Future Outright** Backend Microservice | `fm-hfo` | Calculates historic future outright values. | |
| **Formula Historic Future Two Leg Spread** Backend Microservice | `fm-hftls` | Calculates historic future two leg spread values. | |
| **Formula Historic Future Equity Spread** Backend Microservice | `fm-hfes` | Calculates historic future equity spread values. | |
| **Real-Time Provider** Backend Microservice | `rtp` | Provides real-time data. | |
| **Real-Time Process** Backend Microservice | `rtprc` | Processes real-time data. | |
| **Real-Time Nodejs** Backend Microservice | `rtn` | Handles real-time processing using Node.js. | |
| **Formula Group Trade Equity Outright** Backend Microservice | `fm-geo` | Calculates group trade equity outright values. | |
| **Formula Group Trade Two Leg Spread** Backend Microservice | `fm-getls` | Calculates group trade two leg spread values. | |
| **Formula Group Trade Future Outright** Backend Microservice | `fm-gfo` | Calculates group trade future outright values. | |
| **Formula Group Trade Future Two Leg Spread** Backend Microservice | `fm-gftls` | Calculates group trade future two leg spread values. | |
| **Formula Group Trade Future Equity Spread** Backend Microservice | `fm-gfes` | Calculates group trade future equity spread values. | |
| **Historic Chart** Backend Microservice | `hc` | Generates historic charts. | |
| **Analyst Strategy Information** Backend Microservice | `asi` | Provides information about analyst strategies. | |
| **Formula Historic Equity Outright** Backend Microservice | `fm-heo` | Calculates historic equity outright values. | |
| **Historic Equity Data** Backend Microservice | `hed` | Stores and manages historic equity data. | |
| **Formula Historic Equity Two Leg Spread** Backend Microservice | `fm-hetls` | Calculates historic equity two leg spread values. | |
| **Formula Widget Equity Outright** Backend Microservice | `fm-weo` | Calculates widget equity outright values. | |
| **Formula Widget Equity Two Leg Spread** Backend Microservice | `fm-wetls` | Calculates widget equity two leg spread values. | |
| **Formula Widget Future Two Leg Spread** Backend Microservice | `fm-wftls` | Calculates widget future two leg spread values. | |
| **Formula Widget Future Equity Spread** Backend Microservice | `fm-wfes` | Calculates widget future equity spread values. | |
| **Formula Symbol Equity Spread** Backend Microservice | `fm-ses` | Calculates formula symbol equity spread. | |

<h2 id="Sambar-Frontend-and-UI-Microservices">Sambar Frontend and UI Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| **Site Static Page** Frontend Microservice | `ssp` | Handles static pages of the website. | |
| **User Board** Frontend Microservice | `ub` | Provides the user board interface. | |
| **Add LeBar Form** Frontend Microservice | `alf` | Provides the form for adding LeBar. | |
| **T-Input UI** Frontend Microservice | `tu` | Provides the T-Input user interface. | |
| **Widget Equity Two Leg Spread** Frontend Microservice | `wetls` | Provides the widget for equity two leg spread. | |
| **Widget Future Outright Seasonal** Frontend Microservice | `wfos` | Provides the widget for future outright seasonal data. | |
| **Widget Future Two Leg Spread** Frontend Microservice | `wftls` | Provides the widget for future two leg spread. | |
| **Widget Future Stock Spread** Frontend Microservice | `wfss` | Provides the widget for future stock spread. | |
| **Widget Natural Gas Term** Frontend Microservice | `wngt` | Provides the widget for natural gas term. | |
| **Widget Gasoline RB Term** Frontend Microservice | `wgrbt` | Provides the widget for gasoline RB term. | |
| **Widget Heating Oil Term** Frontend Microservice | `whot` | Provides the widget for heating oil term. | |
| **Widget Brent Crude Oil Term** Frontend Microservice | `wbcot` | Provides the widget for Brent Crude Oil term. | |
| **Widget WTI Crude Oil Term** Frontend Microservice | `wwticot` | Provides the widget for WTI Crude Oil term. | |
| **Widget Symbol Overview** Frontend Microservice | `wso` | Provides an overview of symbols. | |
| **Widget Symbol History Overview** Frontend Microservice | `wsho` | Provides an overview of symbol history. | |
| **Article Portal Board** Frontend Microservice | `apb` | Provides the article portal board. | |
| **Analyst Board** Frontend Microservice | `ab` | Provides the analyst board interface. | |
| **Symbol** Frontend Microservice | `sym` | Manages symbols. | |
| **Widget Ticker** Frontend Microservice | `wt` | Provides the widget ticker. | |

<h2 id="Sambar-Data-and-Content-Management-Microservices">Sambar Data and Content Management Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| Analyst Article CMS Backend Microservice | `aac` | Manages analyst articles. | |
| Article Portal Backend Microservice | `ap` | Handles article portal functionality. | |

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Microservice Catalog for the Sambar/LeBar/k8or Web Applications |
| | Description | This document serves as a comprehensive catalog of all frontend and backend microservices deployed within the Sambar/LeBar/k8or web applications. It provides a centralized repository of information about each microservice. |
| | Identification | TBD | |
| | Version | v0-0-01 | |
| | Format | md | |
| | Revision | This is the first version uploaded to the ChatBOT. |
| | Author | Anna/Barb.Rock |
| | Date | October 14, 2024 |
| Subject Metadata | Alias | TBD |
| |  Name | TBD |
| |  FQID | TBD |
| |  Version | s0-0-01 |
| |  Action | 000010 |
| hGraph Metadata | Alias | none |
| |  Name | none |
| |  FQID | none |
| |  Version | none |
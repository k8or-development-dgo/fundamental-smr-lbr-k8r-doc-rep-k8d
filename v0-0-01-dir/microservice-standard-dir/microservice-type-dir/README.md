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
| **User Authentication** Backend Microservice | `ua` | Handles user authentication and authorization. | `f2b3` `f2b6` `f3b3` `f3b6` `f3b12` `f3b18` `f4b3` `f5b3` `f5b9` `f7b3` `f7b6` `f7b9` `f12b6` `f13b3` `f16b30` `f25b3` `f26b3` |
| **User Invitation** Backend Microservice | `ui` | Manages user invitations. | `f2b9` |
| **User SMS Notification** Backend Microservice | `usn` | Sends SMS notifications to users. | `f2b15` `f3b15` `f4b12` `f5b9` `f6b9` `f7b12` `f7b24` `f7b36` `f13b9` `f16b24` `f16b33` `f16b51` `f25b9` `f25b15` `f26b3` `f26b9` |
| **User Information Payload** Backend Microservice | `uip` | Stores and manages user information. | `f2b12` |
| **User Payload Event Log** Backend Microservice | `upel` | Logs user payload events. | `f3b6` `f3b15` `f3b18` `f4b9` `f5b3` `f7b6` `f7b12` |
| **Authorization** Backend Microservice | `auth` | Handles authorization for different actions. | `f11b3` `f12b3` `f14b3` `f27b3` `f27b6` `f27b9` `f27b12` `f27b15` |
| **Analyst Authentication** Backend Microservice | `aa` | Handles analyst authentication and authorization. | `f51b3` `f51b6` `f51b12` |
| **Analyst Invitation** Backend Microservice | `ai` | Manages analyst invitations. | `f51b9` |
| **Analyst SMS Notification** Backend Microservice | `asn` | Sends SMS notifications to analysts. | `f51b15` |

<h2 id="Sambar-Subscription-and-Payment-Microservices">Sambar Subscription and Payment Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| **Subscription** Backend Microservice | `sub` | Manages user subscriptions. | `f3b3` `f4b9` `f5b3` `f5b4` `f5b6` `f5b12` `f7b18` `f7b21` `f7b27` `f13b6` |
| **Credit Total** Backend Microservice | `ct` | Calculates and manages user credit totals. | `f4b6` `f5b4` `f7b18` `f7b33` `f10b3` `f12b6` `f13b3` |
| **LeBar Total** Backend Microservice | `lt` | Calculates and manages LeBar totals. | `f4b6` `f5b6` `f6b3` `f7b18` `f7b30` `f7b33` `f10b3` `f12b9` `f13b6` `f16b33` `f16b39` `f16b42` `f16b45` `f16b48` `f25b6` `f26b6` |
| **LeBar Cent Information** Backend Microservice | `lci` | Provides information about LeBar cents. | `f4b6` `f7b18` `f7b27` `f7b39` `f10b3` `f12b9` |
| **Add LeBar** Backend Microservice | `al` | Adds LeBar to user accounts. | `f6b3` `f6b6` |
| **Move LeBar** Backend Microservice | `ml` | Moves LeBar between different accounts or purposes. | `f7b30` `f7b33` |
| **Cent to LeBar** Backend Microservice | `ctl` | Converts cents to LeBar. | `f16b48` `f16b51` |
| **Credit Distribution** Backend Microservice | `cd` | Distributes credit among users. | `f12b9` |
| **Convert Credit Event Log** Backend Microservice | `ccel` | Logs credit conversion events. | `f13b3` |
| **User Board Notification** Backend Microservice | `ubn` | Handles user board notifications. | `f7b15` |

<h2 id="Sambar-Trade-Execution-and-Management-Microservices">Sambar Trade Execution and Management Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| **Trade Order** Backend Microservice | `to` | Manages trade orders. | `f7b45` |
| **T-Input Logic** Backend Microservice | `tl` | Handles T-Input logic for trades. | `f9b3` `f9b6` |
| **Strategy Search Data** Backend Microservice | `ssd` | Stores and manages strategy search data. | `f11b3` |
| **Strategy Subscription Event Log** Backend Microservice | `ssel` | Logs strategy subscription events. | `f11b3` |
| **Trade Data** Backend Microservice | `td` | Stores and manages trade data. | `f11b6` `f11b9` `f12b3` `f12b12` `f14b3` `f14b15` `f14b21` `f14b27` `f16b15` `f16b18` `f16b21` `f27b9` `f27b12` `f27b15` |
| **Group Trade Logic** Backend Microservice | `gtl` | Handles group trade logic. | `f12b6` `f16b3` `f16b6` `f16b9` `f16b12` `f16b15` `f16b18` `f16b21` `f16b24` `f16b27` `f25b3` `f25b6` `f25b12` `f26b3` `f26b6` `f27b3` `f27b6` `f27b9` `f27b12` `f27b15` |
| **Group Trade Widget Logic** Backend Microservice | `gtwl` | Provides widget logic for group trades. | `f16b9` `f16b12` `f16b15` `f16b18` `f16b21` `f26b12` `f27b3` `f27b6` `f27b9` `f27b12` `f27b15` |
| **Group Trade Transaction Identification** Backend Microservice | `gtti` | Manages group trade transaction IDs. | `f16b30` `f25b3` `f26b3` |
| **Group Trade Unwind** Backend Microservice | `gtuw` | Unwinds group trades. | `f16b33` |
| **Group Trade Profit** Backend Microservice | `gtp` | Calculates group trade profits. | `f16b39` |
| **Group Trade Fee Penalty** Backend Microservice | `gtfp` | Calculates group trade fee penalties. | `f16b42` |
| **Group Trade Loss** Backend Microservice | `gtls` | Calculates group trade losses. | `f16b45` |
| **Group Trade Wind** Backend Microservice | `gtw` | Manages group trade wind. | `f25b6` `f26b6` |
| **Unwind Profit Loss** Distribution Backend Microservice | `uwpld` | Handles unwind profit loss distribution. | `f16b30` `f16b36` |
| **Demo Trade Equity Outright** Backend Microservice | `deo` | Provides a demo for equity outright trades. | `f18b3` |
| **Demo Trade Equity Two Leg Spread** Backend Microservice | `detls` | Provides a demo for equity two leg spread trades. | `f18b6` |
| **Demo Trade Future Outright** Backend Microservice | `dfo` | Provides a demo for future outright trades. | `f18b9` |
| **Demo Trade Future Two Leg Spread** Backend Microservice | `dftls` | Provides a demo for future two leg spread trades. | `f18b12` |
| **Demo Trade Future ETF Spread** Backend Microservice | `dfetfs` | Provides a demo for future ETF spread trades. | `f18b15` |
| **Demo Trade Future ETN Spread** Backend Microservice | `dfetns` | Provides a demo for future ETN spread trades. | `f18b18` |

<h2 id="Sambar-Data-Processing-and-Analytics-Microservices">Sambar Data Processing and Analytics Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| **Trade Data Verify** Backend Microservice | `tdv` | Verifies trade data. | `f14b12` `f14b18` `f14b24` `f18b9` `f18b12` `f18b15` `f18b18` |
| **Historic Average** Backend Microservice | `ha` | Calculates historic averages. | `f14b12` `f14b18` `f14b24` `f18b9` `f18b12` |
| **Strategy Data** Backend Microservice | `sd` | Stores and manages strategy data. | `f12b12` |
| **Strategy Statistic** Backend Microservice | `ss` | Calculates strategy statistics. | `f14b12` `f14b18` `f14b24` `f18b12` |
| **Historic Future Data** Backend Microservice | `hfd` | Stores and manages historic future data. | `f14b15` `f14b21` `f14b27` `f16b15` `f16b18` `f16b21` `f17b12` `f17b15` `f17b18` `f17b42` `f18b9` `f18b12` `f18b15` `f18b18` `f19b3` `f27b9` `f27b12` `f27b15` |
| **Formula Historic Future Outright** Backend Microservice | `fm-hfo` | Calculates historic future outright values. | `f14b15` |
| **Formula Historic Future Two Leg Spread** Backend Microservice | `fm-hftls` | Calculates historic future two leg spread values. | `f14b21` |
| **Formula Historic Future Equity Spread** Backend Microservice | `fm-hfes` | Calculates historic future equity spread values. | `f14b27` |
| **Real-Time Provider** Backend Microservice | `rtp` | Provides real-time data. | `f15b3` `f17b3` |
| **Real-Time Process** Backend Microservice | `rtprc` | Processes real-time data. | `f15b6` |
| **Real-Time Nodejs** Backend Microservice | `rtn` | Handles real-time processing using Node.js. | `f15b9` |
| **Formula Group Trade Equity Outright** Backend Microservice | `fm-geo` | Calculates group trade equity outright values. | `f16b9` `f27b3` |
| **Formula Group Trade Two Leg Spread** Backend Microservice | `fm-getls` | Calculates group trade two leg spread values. | `f16b12` `f27b6` |
| **Formula Group Trade Future Outright** Backend Microservice | `fm-gfo` | Calculates group trade future outright values. | `f16b15` `f27b9` |
| **Formula Group Trade Future Two Leg Spread** Backend Microservice | `fm-gftls` | Calculates group trade future two leg spread values. | `f16b18` `f27b12` |
| **Formula Group Trade Future Equity Spread** Backend Microservice | `fm-gfes` | Calculates group trade future equity spread values. | `f16b21` `f27b15` |
| **Historic Chart** Backend Microservice | `hc` | Generates historic charts. | `f14b3` `f14b6` `f14b9` `f14b15` `f14b21` `f14b27` `f15b9` `f16b9` `f16b12` `f16b15` `f16b18` `f16b21` `f17b6` `f17b9` `f17b12` `f17b15` `f17b18` `f27b3` `f27b6` `f27b9` `f27b12` `f27b15` |
| **Analyst Strategy Information** Backend Microservice | `asi` | Provides information about analyst strategies. | `f14b6` `f14b9` `f14b15` `f14b18` `f14b24` `f18b3` `f18b6` `f18b9` `f18b12` `f18b15` `f18b18` |
| **Formula Historic Equity Outright** Backend Microservice | `fm-heo` | Calculates historic equity outright values. | `f14b6` |
| **Historic Equity Data** Backend Microservice | `hed` | Stores and manages historic equity data. | `f14b6` `f14b9` `f14b27` `f16b9` `f16b12` `f16b21` `f17b6` `f17b9` `f17b18` `f17b39` `f17b42` `f18b3` `f18b6` `f18b15` `f18b18` `f19b3` `f27b3` `f27b6` |
| **Formula Historic Equity Two Leg Spread** Backend Microservice | `fm-hetls` | Calculates historic equity two leg spread values. | `f14b9` |
| **Formula Widget Equity Outright** Backend Microservice | `fm-weo` | Calculates widget equity outright values. | `f17b6` |
| **Formula Widget Equity Two Leg Spread** Backend Microservice | `fm-wetls` | Calculates widget equity two leg spread values. | `f17b9` |
| **Formula Widget Future Two Leg Spread** Backend Microservice | `fm-wftls` | Calculates widget future two leg spread values. | `f17b15` |
| **Formula Widget Future Equity Spread** Backend Microservice | `fm-wfes` | Calculates widget future equity spread values. | `f17b18` |
| **Formula Symbol Equity Spread** Backend Microservice | `fm-ses` | Calculates formula symbol equity spread. | `f19b3` |
| **Formula Widget Future Outright** Backend Microservice | `fm-wfo` | Calculates formula widget future outright. | `f17b12` |
| **Formula Demo Trade Equity Outright** Backend Microservice | `fm-deo` | Calculates formula demo trade equity outright. | `f18b3` |
| **Formula Demo Trade Equity Two Leg Spread** Backend Microservice | `fm-detls` | Calculates formula demo trade equity two leg spread. | `f18b6` |
| **Formula Demo Trade Future Outright** Backend Microservice | `fm-dfo` | Calculates formula demo trade future outright. | `f18b9` |
| **Formula Demo Trade Future Two Leg Spread** Backend Microservice | `fm-dftls` | Calculates formula demo trade future two leg spread. | `f18b12` |
| **Formula Demo Trade Future Equity Spread** Backend Microservice | `fm-dfes` | Calculates formula demo trade future equity spread. | `f18b15` `f18b18` |

<h2 id="Sambar-Frontend-and-UI-Microservices">Sambar Frontend and UI Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| **Site Static Page** Frontend Microservice | `ssp` | Handles static pages of the website. | `f1b3` |
| **User Board** Frontend Microservice | `ub` | Provides the user board interface. | `f2b3` |
| **Add LeBar Form** Frontend Microservice | `alf` | Provides the form for adding LeBar. | `f6b3` |
| **T-Input UI** Frontend Microservice | `tu` | Provides the T-Input user interface. | `f9b3` |
| **Widget Equity Outright** Frontend Microservice | `weo` | Displays widget equity outright values. | `f17b6` |
| **Widget Equity Two Leg Spread** Frontend Microservice | `wetls` | Provides the widget for equity two leg spread. | `f17b9` |
| **Widget Future Outright Seasonal** Frontend Microservice | `wfos` | Provides the widget for future outright seasonal data. | `f17b12` |
| **Widget Future Two Leg Spread** Frontend Microservice | `wftls` | Provides the widget for future two leg spread. | `f17b15` |
| **Widget Future Stock Spread** Frontend Microservice | `wfss` | Provides the widget for future stock spread. | `f17b18` |
| **Widget Natural Gas Term** Frontend Microservice | `wngt` | Provides the widget for natural gas term. | `f17b24` |
| **Widget Gasoline RB Term** Frontend Microservice | `wgrbt` | Provides the widget for gasoline RB term. | `f17b27` |
| **Widget Heating Oil Term** Frontend Microservice | `whot` | Provides the widget for heating oil term. | `f17b30` |
| **Widget Brent Crude Oil Term** Frontend Microservice | `wbcot` | Provides the widget for Brent Crude Oil term. | `f17b33` |
| **Widget WTI Crude Oil Term** Frontend Microservice | `wwticot` | Provides the widget for WTI Crude Oil term. | `f17b36` |
| **Widget Symbol Overview** Frontend Microservice | `wso` | Provides an overview of symbols. | `f17b39` |
| **Widget Symbol History Overview** Frontend Microservice | `wsho` | Provides an overview of symbol history. | `f17b42` |
| **Article Portal Board** Frontend Microservice | `apb` | Provides the article portal board. | `f23b3` |
| **Analyst Board** Frontend Microservice | `ab` | Provides the analyst board interface. | `f51b3` |
| **Symbol** Frontend Microservice | `sym` | Manages symbols. | `f19b3` |
| **Widget Ticker** Frontend Microservice | `wt` | Provides the widget ticker. | `f17b3` |
| **Unwind Profit Loss** Distribution Frontend Microservice | `uwpld` | Handles unwind profit loss distribution. | `f16b30` |

<h2 id="Sambar-Data-and-Content-Management-Microservices">Sambar Data and Content Management Microservices</h2>

| Microservice Name | Abbreviation | Description | Used |
|---|---|---|---|
| Analyst Article CMS Backend Microservice | `aac` | Manages analyst articles. | `f2b12` `f3b9` `f3b12` `f4b9` `f7b3` `f7b9` `f7b42` `f10b3` `f10b6` `f10b9` `f51b12` |
| Article Portal Backend Microservice | `ap` | Handles article portal functionality. | `f23b3` |

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
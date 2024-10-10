## Sambar/LeBar/k8or Onboarding and Time Management Guidelines

This document outlines the essential procedures for new team members joining the Sambar/LeBar/k8or environment to ensure smooth onboarding and efficient time management.

## Content

1. **[Obtaining a JIRA Ticket](#Obtaining-a-JIRA-Ticket)**
2. **[Time Tracking with Toggl](#Time-Tracking-with-Toggl)**
3. **[JIRA Ticket Status Management](#JIRA-Ticket-Status-Management)**
4. **[JIRA Ticket Commenting](#JIRA-Ticket-Commenting)**
5. **[k8or JIRA Sprint Naming Convention](#k8or-JIRA-Sprint-Naming-Convention)**
6. **[Document Metadata](#Document-Metadata)**

<h1 id="Obtaining-a-JIRA-Ticket">Obtaining a JIRA Ticket</h1>

* **Requirement:** Every task, whether studying or actively working, requires a JIRA ticket. No work can be performed without a designated ticket.
* **Process:** Upon joining the company, acquire a ticket from a designated individual.

<h1 id="Time-Tracking-with-Toggl">Time Tracking with Toggl</h1>

* **Importance:** We utilize Toggl to track time spent on assigned JIRA tickets.
* **Instructions:**
    1. Track your time on the JIRA ticket using Toggl Desktop application.
    2. Paste the following text into the Toggl description box:  
       ```
       [Your Ticket ID] [Your Ticket Title]
       ``` 
       ```
       K8RT-1 Sambar/LeBar/k8or Architecture and Kubernetes Fundamentals
       ```
    3. Stop the Toggl timer whenever you are not actively working on the ticket.

<h1 id="JIRA-Ticket-Status-Management">JIRA Ticket Status Management</h1>

* **Start Status:** When you begin working on a ticket, update its status to `In Progress`.
* **Completion Status:** Upon finishing work on a ticket, update its status to `Done`.

<h1 id="JIRA-Ticket-Commenting">JIRA Ticket Commenting</h1>

* **Start Comment:** Upon initiating work on a ticket, leave the first comment with the start date and time in the following format:
   ```
   Start: 10:30 IST, October 10, 2024
   ```
* **End Comment:** When you finish working on a ticket, leave a final comment with the end date and time in the following format:
   ```
   End: 17:30 IST, October 10, 2024
   ```

<h1 id="k8or-JIRA-Sprint-Naming-Convention">k8or JIRA Sprint Naming Convention</h1>

**Purpose:** The k8or JIRA sprint naming convention is designed to provide a clear and concise identifier for each sprint, making it easy to track and manage project progress.

**Structure:**

A k8or JIRA sprint name follows the following format:

```
w[week_number]-y[year]-k8d: [sprint_name]
```

**Components:**

1. **`w[week_number]`:** Two-digit number, such as 01, 02, ..., 41, represents the week number within the current year. For example, `w41` indicates the 41st week of the year.
2. **`y[year]`:** Two-digit number indicates the year in which the sprint is taking place. For example, `y24` denotes the year 2024.
3. **`k8d`:** This is a unique identifier for the k8or development environment.
4. **`:`:** A colon separates the numerical components from the sprint name.
5. **`[sprint_name]`:** This is a user-friendly, memorable name given to the sprint. It should be descriptive and relevant to the sprint's goals or focus.

**Example:**

`w41-y24-k8d: brave-spirit`

* **`w41`:** Week 41 of the year
* **`y24`:** Year 2024
* **`k8d`:** k8or development environment
* **`brave-spirit`:** User-friendly sprint name

**Key Points:**

* The components in the sprint name are separated by hyphens and a colon with a space after the colon.
* The sprint name should be unique and easily recognizable.
* Adhering to this naming convention ensures consistent and informative sprint identification within the k8or project.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Sambar/LeBar/k8or Onboarding and Time Management Guidelines |
| | Description | This document outlines the essential procedures for new team members joining the Sambar/LeBar/k8or environment to ensure smooth onboarding and efficient time management. |
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
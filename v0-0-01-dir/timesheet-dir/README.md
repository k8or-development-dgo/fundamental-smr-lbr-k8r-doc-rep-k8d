# Understanding the Weekly Timesheet Structure within the Sambar/LeBar/k8or Web Applications

This document provides a comprehensive guide to the structure and conventions used in weekly timesheet files within the Sambar/LeBar/k8or web applications. It serves as a reference for understanding the data format, naming conventions, and intended use of these files.

## Content

1. **[Introduction](#Introduction)**
2. **[File Naming Convention](#File-Naming-Convention)**
3. **[File Structure](#File-Structure)**
4. **[Data Format](#Data-Format)**
5. **[Mini-Break Tracking](#Mini-Break-Tracking)**
6. **[Additional Notes](#Additional-Notes)**
7. **[Download Weekly Timesheet Template](#Download-Weekly-Timesheet-Template)**
8. **[Document Metadata](#Document-Metadata)**

<h1 id="Introduction">Introduction</h1>

The timesheet serves as a critical tool for tracking team member attendance, calculating wages, and scheduling AWS EC2 instance start times within the Sambar/LeBar/k8or web applications. It provides a structured record of a team member's work hours, including planned and actual timings, breaks, and total hours worked. This information is essential for accurate payroll calculations, resource allocation, and ensuring efficient operations.

![Alt text](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/blob/k8or-dev/v0-0-01-dir/timesheet-dir/example-dir/timesheet-example-v0-0-01-fil.png)

<h1 id="File-Naming-Convention">File Naming Convention</h1>

The filename follows a consistent format: `[Name]-[Weekly Timesheet]-[Start Date]`. For example, `anna-veretennykova-weekly-timesheet-monday-october-7-2024`.

<h1 id="File-Structure">File Structure</h1>

The timesheet is organized into two main sections:

1. **Planned Schedule:**
   - **Header:** Includes the team member's name, the week starting date, city, and a note about using UTC military time.
   - **Planned Hours:** Lists the planned workdays, start and end times, break durations, and total hours.
   - **Total Hours per Week:** Displays the total planned working hours for the week.

2. **Actual Timing:**
   - **Header:** Similar to the planned schedule header, but with the addition of `Actual Timing`.
   - **Actual Hours:** Lists the actual workdays, start and end times, break durations, number of mini-breaks, and total hours worked.
   - **Total Hours per Week:** Displays the total actual working hours for the week.

<h1 id="Data-Format">Data Format</h1>

- **Date:** Uses the format `MM/DD/YYYY`.
- **Type:** Indicates the day type, either `R` for regular workday or `A` for absent.
- **Time In/Out:** Uses 24-hour format (e.g., `05:00` for 5 AM).
- **Break:** Specifies the break duration in minutes.
- **Total Hours:** Calculates the total working hours for each day and the week.


<h1 id="Mini-Break-Tracking">Mini-Break Tracking</h1>

The timesheet includes a column for `Number of M-Breaks` to track short breaks or `mini-breaks` taken throughout the day. These mini-breaks are not explicitly listed in the planned or actual timing sections. Instead, the number of mini-breaks taken on each day is recorded in the column `Number of M-Breaks`.

<h1 id="Additional-Notes">Additional Notes</h1>

- The timesheet is used to track team member attendance, calculate wages, and schedule AWS EC2 instance start times.
- The `Number of M-Breaks` column might be used to track short breaks or `mini-breaks` taken throughout the day.
- The `Actual Timing` section allows for comparison between planned and actual working hours, identifying any discrepancies or adjustments.
- The timesheet integrates with AWS EventBridge to automate the scheduling of EC2 instance start times based on the recorded working hours.
- **Caution: When updating the timesheet template, be careful not to delete or modify any existing formulas. These formulas are critical for accurately calculating working hours and totals.**

<h1 id="Download-Weekly-Timesheet-Template">Download Weekly Timesheet Template</h1>

- The weekly timesheet template can be downloaded from the `timesheet-dir/template-dir` GitHub repository directory: **[download template](https://github.com/k8or-development-dgo/fundamental-smr-lbr-k8r-doc-rep-k8d/tree/k8or-dev/v0-0-01-dir/timesheet-dir/template-dir)**. 
- **Remember to use caution when modifying the template to avoid disrupting the formulas used for calculating working hours.**

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | Understanding the Weekly Timesheet Structure within the Sambar/LeBar/k8or Web Applications |
| | Description | This document provides a comprehensive guide to the structure and conventions used in weekly timesheet files within the Sambar/LeBar/k8or web applications. It serves as a reference for understanding the data format, naming conventions, and intended use of these files. |
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
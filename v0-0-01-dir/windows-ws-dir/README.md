## k8or Windows-WS Security and Management

This document outlines the security measures, automated management processes, and connection procedures for the k8or Windows-WS instances.

## Content

1. **[Security Measures](#Security-Measures)**
2. **[Automated Workspace Management](#Automated-Workspace-Management)**
3. **[IP Address Restrictions](#IP-Address-Restrictions)**
4. **[Connecting to a k8or Windows-WS](#Connecting-to-a-k8or-Windows-WS)**
5. **[Document Metadata](#Document-Metadata)**

<h1 id="Security-Measures">Security Measures</h1>

* **Individual Windows-WS Instances:** Each k8or team member is provisioned with a dedicated Windows-WS instance running on the AWS cloud platform. This isolation enhances security by preventing unauthorized access to sensitive data and resources.
* **Robust Security Rules:** Multiple security rules are implemented within the k8or Windows-WS workspaces to safeguard against potential threats. These rules include:

  * Network access controls
  * Firewall configurations
  * User authentication and authorization policies

<h1 id="Automated-Workspace-Management">Automated Workspace Management</h1>

* **Daily Start-Up:** To optimize resource utilization and security, a scheduled AWS EventBridge trigger is configured for each k8or team member. This trigger activates a custom Lambda function that starts the corresponding Windows-WS instance 15 minutes before the start of the workday.
* **Daily Shut-Down:** Another EventBridge trigger is set up to initiate a custom Lambda function that stops the Windows-WS instance at a predetermined time at the end of the workday. This ensures that the workspace is only active during working hours, minimizing exposure to potential vulnerabilities.

<h1 id="IP-Address-Restrictions">IP Address Restrictions</h1>

* **Access Control:** To further enhance security, the k8or Windows-WS workspaces are configured to allow access only from specific IP addresses. This restricts access to authorized individuals and prevents unauthorized remote connections.
* **IP Address Notification:** It is essential for each team member to provide their local IP address to the k8or team. This information is used to update the workspace's access control rules, ensuring that the team member can connect to their Windows-WS instance seamlessly.
* **Access Denial:** Failure to provide the correct local IP address will result in denied access to the workspace, preventing unauthorized access and potential security breaches.

<h1 id="Connecting-to-a-k8or-Windows-WS">Connecting to a k8or Windows-WS</h1>

**1. Obtain Credentials:**
   * Receive the following credentials from a k8or team member:
     - Computer IP address
     - Computer name
     - Username
     - Password

**2. Secure Credentials:**
   * Store the credentials in a secure location on your local Windows-WS to prevent unauthorized access.

**3. Locate RDP Application:**
   * Go to the search bar on your local Windows-WS.
   * Search for `RDP` (Remote Desktop Protocol).
   * Select the RDP application from the search results.

**4. Create a New RDP Session:**
   * A new window will open for a new RDP session.

**5. Enter Computer IP:**
   * In the `Computer` field, enter the IP address provided by the k8or team member.

**6. Expand Options and Enter Username:**
   * Click on the `Show options` button in the left corner to expand the options.
   * In the `User name` field, enter the username provided by the k8or team member in the following format:

     ```
     computer_name\username
     ```

     Replace `computer_name` with the actual `computer name` and `username` with the given username.

**7. Always Ask for Credentials:**
   * Check the `Always ask for credentials` box to ensure you are prompted for the password each time you connect.

**8. Connect to the k8or Workspace:**
   * Click on the `Connect` button.
   * Enter the password provided by the k8or team member.
   * Check the `Remember me` box for convenience.

**9. Successful Login:**
   * Once the connection is established, you will be logged in to the k8or Windows-WS.

---

<h2 id="Document-Metadata">Document Metadata</h2>

| Metadata Type | Key | Value |
|---|---|---|
| Document Metadata | Title | k8or Windows-WS Security and Management |
| | Description | This document outlines the security measures, automated management processes, and connection procedures for the k8or Windows-WS instances. |
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
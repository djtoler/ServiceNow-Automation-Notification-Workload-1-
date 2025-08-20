# Urgent Incident Notification Workflow (Workflow 1)

## System Overview

##### This system automates the notification process for critical network incidents. We use ServiceNow's Flow Designer workflow to monitor newly created or updated incidents. 
##### When an incident has a "Network" category and a "Critical" priority, the workflow automatically sends an immediate email to the 
##### Network Operations team. 

## Implementation Steps

1.  ** A update set named "w01UrgentIncidentNotification" was created to capture configuration changes.
2.  **A new user group named "Network Operations" was created to recieve critical incident notifications.
3.  **In flow designer, "Kura Workload 1" flow was renamed to "Urgent Notification for Network Operations Incidents." The trigger was configured to run when an Incident is created or updated, with conditions set to **Category is Network** and **Priority is 1 - Critical**.
4.  **An action was added to the flow to send an email notification. 
5.  **A test incident was created with a "Network" category, and high impact/urgency to trigger & verify the workflow. 
6.  **The update set was exported to an XML file.

## Architecture Diagram

![Architecture Diagram](https://github.com/djtoler/ServiceNow-Automation-Notification-Workload-1-/blob/main/service-now-urgent-incident-notification-workflow/Diagram.png)

## AI Scenario

An AI agent would enhance this incident routing system by implementing intelligence at the decision making points rather than conditions. An agent can read details and semantically 
compare it to other past incidents and decide more intelligently how to catagorize and prioritize incidents. Agents may also implement solutions faster than a human, which would help 
protect SLAs. It would also be able to send relevant documentation to the recipient(s) to push for a faster resolution. AI agents would offer more personalized emaails and based off of contextual data, could possible send the emails to the right select individuals within the assigned group, somthing a deterministic system may struggle to do without all well thought-out scenarios accounted for, where as an agent implementation is usefully dynamic

# Operational-Ticket-Monitoring-And-Escalation-System

## Overview

This project simulates an operational workflow system designed to track, prioritize, and respond to internal requests in a structured and automated way.

It demonstrates how business rules, data tracking, and reporting logic can be implemented using Microsoft Power Platform tools.

The system improves visibility and response time for high-priority operational requests by automating detection and escalation workflows.

## System Architecture

- SharePoint List → Structured intake and data storage
- Power Automate → Business rules engine and workflow automation
- Teams / Email Notifications → Real-time alerts and escalation messaging

## Key Features
Business Problem

Internal operational requests lacked structured prioritization and required manual monitoring, leading to delays in identifying high-priority items.


Solution

Implemented an automated intake + escalation workflow using SharePoint and Power Automate to improve visibility and response time.


Structured Ticket Intake
![Support Ticket Tracker List](https://raw.githubusercontent.com/AOseni1/Operational-Ticket-Monitoring-And-Escalation-System/main/Images/Sharepoint_List.png)
Tracks operational requests with fields including:
- Title
- Priority (Low / Medium / High)
- Status (New, In Progress, Closed)
- Category

Ticket Creation

![Adding a new item to the list](https://raw.githubusercontent.com/AOseni1/Operational-Ticket-Monitoring-And-Escalation-System/main/Images/Adding_Policy_Ticket.png)

Users can submit new operational requests directly into the SharePoint list.

## Automated Priority Detection

Power Automate evaluates incoming tickets and identifies High priority items for escalation.
![Automatically detects High priority tickets](https://raw.githubusercontent.com/AOseni1/Operational-Ticket-Monitoring-And-Escalation-System/main/Images/Conditon.png)


## Dynamic Notifications System
When a High priority ticket is detected, the system sends a structured notification including:
- Ticket title
- Status
- Contextual escalation message
  ![Sends dynamic notifications including](https://raw.githubusercontent.com/AOseni1/Operational-Ticket-Monitoring-And-Escalation-System/main/Images/FlowBot_Actions.png):

## Automated Alert Output

Notifications are delivered in real time via Teams, simulating operational escalation workflows.

![Flowbot Chat](https://raw.githubusercontent.com/AOseni1/Operational-Ticket-Monitoring-And-Escalation-System/main/Images/FlowBot_chat.png)

## Workflow Logic

1. A new ticket is created in the SharePoint list
2. Power Automate evaluates ticket priority
3. If priority = High:
   - Trigger escalation notification
   - Send dynamic ticket details
Include dynamic ticket details
4. Otherwise:
  - No escalation triggered
![Workflow Logic](https://raw.githubusercontent.com/AOseni1/Operational-Ticket-Monitoring-And-Escalation-System/main/Images/Power_Automate_Flow.png)

## Challenges & Learnings

Dynamic Content Handling

- Resolved issues with rendering SharePoint fields (e.g., using Status Value instead of object references)

Conditional Logic Debugging

- Fixed evaluation errors by correctly referencing nested field values in Power Automate expressions.

Connection & Authentication Issues

- Resolved connector failures caused by invalid or unlicensed connections, reinforcing understanding of environment-level constraints.

These challenges reflect common real-world issues when working with enterprise workflow automation tools.

## Outcome

This project demonstrates an end-to-end operational workflow that:

- Reduces manual monitoring effort for high-priority requests
- Improves response time through automated escalation
- Translates business rules into actionable workflow automation

## Future Enhancements

- SLA tracking and time-based escalation
- Power BI dashboard for reporting and trend analysis
- Expanded workflow logic for multi-team routing

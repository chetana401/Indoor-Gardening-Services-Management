# Indoor Gardening Services Management (IGSM)

## Project Overview

Indoor Gardening Services Management (IGSM) is a ServiceNow Scoped Application designed to manage indoor gardening service requests efficiently. The application provides an end-to-end workflow for request creation, automation, SLA tracking, validation, and role-based security.

## Features

* Service Portal request submission
* Record Producer for creating backend request records
* Automated workflow using Flow Designer
* Business Rule for automatic default priority assignment
* Response and Resolution SLA tracking
* Client-side validation
* Role-based Access Control (ACL)
* Technician assignment and request management

## Workflow

User Request → Record Creation → Priority Validation → Manager Approval → Technician Assignment → Notification → Request Completion

## Technologies Used

* ServiceNow
* Flow Designer
* Business Rules
* Record Producers
* Catalog Client Scripts
* Service Level Agreements (SLAs)
* Access Control Lists (ACLs)
* Service Portal

## Business Rule

If the user submits a request without selecting a priority, the system automatically assigns the priority as **Low**.

## Client-Side Validation

When the priority is set to **High**, the Description field becomes mandatory. For Medium and Low priority requests, the Description field remains optional.

## SLA Configuration

### Response SLA

* Duration: 4 Hours
* Starts: State = New
* Stops: State = Assigned

### Resolution SLA

* Duration: 2 Days
* Starts: State = Assigned
* Stops: State = Completed

## Security Roles

| Role       | Access                  |
| ---------- | ----------------------- |
| Requester  | Read and Create         |
| Technician | Read, Create and Update |
| Manager    | Full Access             |

## Learning Outcomes

This project demonstrates practical ServiceNow development concepts including scoped application development, request management, workflow automation, SLA configuration, client-side and server-side scripting, and role-based security.

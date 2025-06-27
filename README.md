# Configuring an IT Ticketing System with Jira

## Overview

Welcome to part 2 of my Active Directory Lab series! Click [here](https://github.com/seanmarcus1/Active-Directory-Lab-Setup) if you haven't checked out part 1 where I set up the AD environment. 

In this lab, we will be simulating a realistic IT service desk workflow by integrating Jira Service Manager into our Windows domain environment. A domain user will submit an internal IT support ticket, and an analyst resolves it through Jira's web interface.



---

## Objectives
- Set up Jira Service Management
- Submit a service request from a domain user
- Respond to and resolve the ticket from an analyst/admin view
- Document and validate the service desk workflow

---

## Lab Environment
- **CLIENT01**: Windows 11 client joined to the Active Directory domain
- **DC01**: Windows Server 2019 Domain Controller
- **Host Mahcine**: Used for hositng the Jira web-based interface

---

### Configuring Jira
- On host machine, sign up for an Atlassian account
- Select Jira Service Management


Configured using 'IT Service Management' template: ![01  Template](https://github.com/user-attachments/assets/48a32536-a4d7-4da1-8d89-0c9328bfd898)

Project creation screen: ![02  Create Project](https://github.com/user-attachments/assets/41f46dcd-7d15-4546-a331-a33c5ecff270)

Main admin view dashboard: ![03  Main Dashboard](https://github.com/user-attachments/assets/55abf993-b1cd-4a66-808d-8ee41344281c)

---

### Creating and Submitting the Ticket
- Flipping over to Windows 11 client machine
- User submits a ticket describing issues with Microsoft Outlook via the Jira portal

Portal from the user's perspective: ![04  User Portal](https://github.com/user-attachments/assets/392b58a6-c3fc-48f3-8c50-80afd3dea65b)

Logged in as 'Steven Roberts' on the client machine: ![05  Login Proof](https://github.com/user-attachments/assets/21402de7-0085-4bb6-ac30-e37f7674abbb)

User creates a ticket detailing how Outlook is crashing and steps already taken on their end: ![07  Ticket Creation](https://github.com/user-attachments/assets/62fa3d30-6a0b-4448-ae30-be55c7fef49e)

Ticket submitted to the analyst with status of 'Waiting For Support': ![06  Ticket Created](https://github.com/user-attachments/assets/c7058158-aa6e-42a9-bb98-98c536a475e6)

---

### Resolving the Ticket
- From the analyst dashboard on host machine, the ticket is received, triaged, and resolved

Ticket received by the analyst: ![08  Ticket Shown on Analyst](https://github.com/user-attachments/assets/15ad0493-ae24-4a67-9195-cd8d25cb3092)

Ticket in detail: ![09  Detailed Ticket](https://github.com/user-attachments/assets/354b943a-c063-4633-be95-882ce8b55b07)

Windows Event viewer showing an error in the Outlook application (simulated for lab purposes): ![outlook error](https://github.com/user-attachments/assets/65085265-3aa9-4db3-9fb4-9be129369590)

Internal troubleshooting note and note to the user created as well as the status of the ticket is changed to 'Resolved': ![10  Notes created and ticket resolved](https://github.com/user-attachments/assets/9744b0eb-bd58-43d2-b813-cc7e3617bcbc)

The user receives communication from the analyst throughout the entire process via email: ![11  Email Chain](https://github.com/user-attachments/assets/070438f1-1193-4f14-8739-671b65c8a1df)

---

### Key Takeaways
- Demonstrated end to end internal ticket resolution.
- Gained experience using Jira Service Management as both the technician who resolves the issue at hand as well as the customer who is going through technical difficulties.
- Reinforced key service desk practices including ticket documentation, escalation restriction, and status handling.

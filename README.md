# 🖨️ Printing Shop — Software Requirement Specifications & Design (SRSD)

> **Course:** Software Engineering (COMP 433)
> **Instructor:** Prof. Adel Taweel
> **Faculty:** Engineering and Technology — Computer Science Department, Birzeit University
> **Group No.:** 1

## 📌 Project Overview

The **Printing Shop** is an existing physical business that accepts print orders from customers and delivers printed copies to their address. It currently operates manually — handling orders in person or by phone — and serves students, individuals, and businesses who need printed materials in different formats, sizes, and colors.

This repository documents the full software engineering lifecycle of building an **online system** for the Printing Shop that allows customers to:

- Upload documents (PDF, DOCX, JPEG, PNG) for printing
- Configure printing preferences (color mode, paper size, copies, etc.)
- Place and pay for print orders (online card payment or cash on delivery)
- Track orders from submission through delivery
- Cancel pending orders, submit support inquiries, and rate completed orders

The project was developed iteratively across **four phases**, following an Agile-based strategy layered on top of the course's required Waterfall-style phase structure (draft → team review → revision → instructor feedback → further revision).

## 👥 Team — Group No. 1

| Name | Student ID | Role |
|---|---|---|
| Dareen Abualhaj | 1220686 | Project Manager |
| Tala Saabneh | 1221464 | Requirement Engineer |
| Razan Froukh | 1222192 | Secretary |
| Taima Nazzal | 1220701 | Programmer |
| Shahd Shwekeyeh | 1222105 | QA & Software Tester |

## 📂 Repository Contents

| File | Description |
|---|---|
| `G1-1220686_Dareen_Abualhaj-phase1-AT.pdf` | **Phase 1** — Business Description (Business overview, services, capacity, employees, business process/model, challenges) |
| `G1-1220686_Dareen_Abualhaj-G1-Phase2-AT.pdf` | **Phase 2** — Requirements Engineering (User Requirements, System Requirements, Effort & Time Estimation) |
| `G1-1220686_Dareen_Abualhaj_-G1-Phase3-AT.pdf` | **Phase 3** — Requirements Analysis and Modelling (Actor Analysis, Use-Case Diagram & Specifications, Activity Diagram) |
| `G1-1220686_Dareen_Abualhaj-G1-Comp433-Final-ProjectReport-AT.pdf` | **Final Phase** — Full SRSD Report (all chapters, including System Design & Modelling, revised based on feedback) |
| `Project_Presentation.pdf` | Final project presentation slides |

## 🗂️ Document Structure (Final Report)

1. **Chapter 1 — Project Planning and Management**
   - Team roles, project management strategy, Project Manager report, individual member reports
2. **Chapter 2 — Requirement Elicitation, Analysis and Modelling**
   - Business description
   - User Requirements (UR1–UR9) & System Requirements (SR1.x–SR9.x)
   - Effort and Time Estimation
   - Actor Analysis, Use-Case Diagram, Use-Case Specifications, Activity Diagram
3. **Chapter 3 — System Analysis and Modelling**
   - Analysis Class Diagram, Detailed Class Diagram, Sequence Diagrams
4. **Chapter 4 — System Design and Modelling**
   - System Design Goals (High Cohesion, Low Coupling, Reliability)
   - Component Diagram, Overall Architecture Diagram, Deployment Diagram
5. **Appendix I** — Minutes of Meetings
6. **Team Member Photos**

## 🎭 Key Actors

| Actor | Type | Description |
|---|---|---|
| Customer | Primary | Uploads documents, configures print options, places/pays for orders, tracks/cancels orders, submits inquiries, rates orders |
| Admin | Primary | Manages accounts, monitors operations, generates business reports |
| PrintOperator | Primary | Processes print jobs, performs quality checks, packages orders |
| SupportStaff | Primary | Handles customer inquiries and escalations |
| FinanceStaff | Primary | Manages payments, refunds, and financial reporting |
| DeliveryCoordinator | Primary | Manages shipment and delivery tracking |
| PaymentSystem | Secondary | External system validating and processing online payments |
| NotificationSystem / Email Service | Secondary | Sends automated order/payment/cancellation notifications |
| SystemTimer | Secondary | Triggers automated reminders (e.g., pending payment) |

## 🏗️ System Architecture

The system follows a **three-tier layered architecture**:

- **Presentation Layer** — Order Placement, Order Tracking, Print Job Management, Inquiry & Support, Finance & Reporting, Delivery Management, and Account Management UIs
- **Domain Layer** — Account & Access, Document & Order, Print Job, Payment, Inquiry & Support, Delivery, Reporting & Analytics, and Finance & Refund Management components
- **Infrastructure Layer** — Payment Gateway Adapter, Notification Gateway, Security, and Persistence services, backed by the Print Shop DB

### Design Goals

1. **High Cohesion** — each class/component owns a single, well-defined responsibility (e.g., `Order` holds order data only; `Payment` owns all transaction logic).
2. **Low Coupling** — components interact via well-defined method calls and status values rather than direct data access, enabling independent replacement (e.g., swapping payment gateways).
3. **Reliability** — atomic order transactions, safe payment state transitions, and full failure logging ensure no partial or inconsistent order/payment data.

## 🔄 Core Use Cases

| ID | Use Case | Actor |
|---|---|---|
| UC1 | Upload Documents | Customer |
| UC2 | Select Printing Options | Customer |
| UC3 | Place Print Order | Customer |
| UC4a/b | Pay by Card / Cash on Delivery | Customer |
| UC5 | Track Order Status | Customer |
| UC6 | Cancel Print Order | Customer |
| UC7 | Submit Inquiry | Customer |
| UC8 | Rate Completed Order | Customer |
| UC9–11 | Generate Reports / Manage Orders & Accounts | Admin |
| UC12–14 | Process Print Job / Quality Check / Package Order | Print Operator |
| UC17–18 | Process Refund / Generate Financial Report | Finance Staff |
| UC19–20 | Assign Delivery / Update Delivery Status | Delivery Coordinator |

## 📅 Development Process

The team followed an **iterative, feedback-driven process**:

1. Requirements elicitation and business analysis meetings with the customer team
2. Multiple internal review cycles for each deliverable (Actor Analysis, Use-Case Diagram, Use-Case Specifications, Activity Diagram, Class Diagrams, Sequence Diagrams, Component/Architecture/Deployment Diagrams)
3. Instructor feedback incorporated and revised across Phases 2, 3, and the Final Phase
4. Minutes of meetings recorded for each customer–developer and internal team session

## 🛠️ Effort & Cost Estimation Summary

- **Team size:** 5 developers
- **Total estimated effort:** 16 person-weeks
- **Estimated schedule:** 13–20.8 weeks (with 30% buffer)
- **Agreed project duration:** 14 weeks
- **Agreed project cost:** $6,000

## 📄 License

This repository is an academic project prepared for the **Software Engineering (COMP 433)** course at Birzeit University. All content is intended for educational purposes.

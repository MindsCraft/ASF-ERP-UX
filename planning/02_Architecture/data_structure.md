# Data Entities & Information Architecture
**Project:** ASF ERP - HRM Module
**Focus:** UI Data Requirements

This document outlines the core data entities and fields required to support the UX design, forms, and information display across the HRM module.

## 1. Core Entities

### 1.1 User Records
*Information required for authentication and access control display.*

| Attribute | UX Purpose | Notes |
| :--- | :--- | :--- |
| **Employee Link** | Profile association | Connects user to their employee profile |
| **Username/Email** | Identity | Primary login identifier |
| **Role** | Access Branding | Enum: ['Super Admin', 'HR Admin', 'Manager', 'Employee', 'Accounts'] |
| **Account Status** | Visibility | Enum: ['Active', 'Inactive', 'Banned'] |
| **Last Login** | Activity status | Shown in user directory |
| **Permissions** | Feature access | Controls visibility of sidebar modules and buttons |

### 1.2 Employee Master Data
*The central data used for profile views and employee directories.*

| Attribute | UX Purpose | Notes |
| :--- | :--- | :--- |
| **Employee ID** | Unique ID display | e.g., ASF-2025-001 |
| **Full Name** | Identity | First Name + Last Name |
| **Contact Info** | Communication | Email and Phone |
| **Organization Details** | Context | Institution (ASF/Madrasatus Sunnah), Branch, Dept, Designation |
| **Reporting Line** | Hierarchy | Direct Supervisor name/link |
| **Employment Status** | Lifecycle | Enum: ['Probation', 'Permanent', 'Intern', 'Volunteer'] |
| **Personal Info** | Demographic | Date of Birth, Blood Group, NID/Passport |
| **Address** | Geography | Present and Permanent addresses |
| **Financial Meta** | Compensation view | Gross Salary and Bank Details (for payroll views) |
| **Media/Assets** | Visuals | Profile Image and Documents (CV/NID) |

---

## 2. Operational Data Requirements

### 2.1 Attendance Data
*Data required for calendar views and daily logs.*

| Attribute | UX Purpose | Notes |
| :--- | :--- | :--- |
| **Log Date** | Calendar placement | ISO Date |
| **Punch Times** | Precision | Check-In and Check-Out timestamps |
| **Daily Status** | Visual coding | Enum: ['Present', 'Absent', 'Late', 'Leave'] |
| **Exception Info** | Alerts | Late minutes calculation |
| **Log Source** | Transparency | Biometric, Manual, or Remote entry |

### 2.2 Leave Requests
*Data required for application forms and approval dashboards.*

| Attribute | UX Purpose | Notes |
| :--- | :--- | :--- |
| **Applicant** | Context | Name of employee applying |
| **Leave Type** | Categorization | Enum: ['Sick', 'Casual', 'Annual', 'Unpaid'] |
| **Duration** | Planning | Start Date, End Date, and Total Days |
| **Reason** | Justification | Text area content |
| **Approval State** | Workflow | Enum: ['Pending', 'Approved_Supervisor', 'Approved_HR', 'Rejected'] |
| **Audit Trail** | Transparency | History of who approved/rejected and when |

### 2.3 Expense Claims
*Data required for reimbursement forms and financial summaries.*

| Attribute | UX Purpose | Notes |
| :--- | :--- | :--- |
| **Category** | Budgeting | Enum: ['Transport', 'Food', 'Purchase', 'Tax'] |
| **Amount** | Financial | Currency value |
| **Claim Date** | Context | Date expense was incurred |
| **Evidence** | Verification | Receipt image/document thumbnails |
| **Status** | Lifecycle | Enum: ['Pending', 'Approved', 'Paid', 'Rejected'] |

### 2.4 Payroll Records
*Data required for payslip generation and salary sheets.*

| Attribute | UX Purpose | Notes |
| :--- | :--- | :--- |
| **Pay Period** | Selection | Year and Month |
| **Earnings Breakdown** | Transparency | Basic, House Rent, Medical, Conveyance, Overtime |
| **Deductions** | Transparency | Tax, Provident Fund, Absences |
| **Net Payable** | Final value | The total amount to be disbursed |
| **Payment Status** | Alert | Enum: ['Unpaid', 'Processed', 'Disbursed'] |

---

## 3. Configuration & Metadata
*   **System Settings:** Organization branding (Logo, Name), API connectivity indicators.
*   **Leave Rules:** Entitlement quotas (e.g., "14 days of Annual Leave").
*   **Public Data:** Shared holiday calendars and notice board announcements.

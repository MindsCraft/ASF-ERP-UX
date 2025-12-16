# Client Requirements Input

> **Instructions:** Please paste any additional client requirement texts, emails, or notes in this file. I will read this file to update the project planning and design documents.

---

## Existing Requirements (SRS v1.0)
*Pasted from chat on 2025-12-15*

© 2025 As-Sunnah Foundation. All rights reserved.
System Requirements Specifications (SRS)
As sunnah Foundation ERP System (Version: New)
SRS Version 1.0 ● 09 December 2025

**1.2 Scope of HRM Module**
To automate daily operation of the As-sunnah foundation we will develop a ERP system which will cover the below modules:
• Human Resource Management System (HRM)
• Training Center Management system (TCMS)
• Accounts Management System (AMS)
• Asset Management System (AMS)
• Charity and Social Service (CSS) Project Management system
• Purchase and Procurement system (PMS)

**Human Resource Management System (HRM) Module:**
The ERP-HRM module for ASF Office serves as a centralized human resource management system that manages complete employee information and automates core HR processes across multiple institutions and branches. The module covers:
• Employee Administration
• Attendance Management
• Leave Management
• Payroll Management
• Provident Fund
• Expense Management
• Notice & Notifications
• User & Security Management

**In Scope:**
• Workforce administration (employee master data, hierarchy, roles, branches, departments, institutions)
• Time and attendance with biometric login/logout tracking
• Leave automation with approval workflows and leave balance tracking
• Monthly payroll including salary breakdown, statutory deductions, arrear, tax, and allowances
• Employee financial contributions (Provident Fund – employer & employee)
• Expense claims and reimbursements with category management and reporting
• Internal engagement & communication (Digital notice board, SMS/email alerts)
• Security and user role governance (role-based authentication, unlimited user creation, profile & password management)

**Scope excludes**
Mobile App
Data analytics like Power BI reporting, ETL Pipeline development

**Users & Roles:**
1. **Super Administrator:** Full access, System Config, User Management.
2. **HR Administrator:** Onboarding, Payroll, Leave, Claims, Policy.
3. **HR Manager/Supervisor:** Team management, Approvals (Leave/Expense).
4. **Accounts/Finance Officer:** Payroll verification, Disbursement, Tax/PF.
5. **Employee:** Self-service (Profile, Leave, Claims, Payslips).

**3. Detailed Functional Requirements (Summary)**
*   **FRS001 User Signup/Login:** SSO, Email/Pass, OTP.
*   **FRS002 HRM Dashboard:** Stats for Employees, Attendance, Leave.
*   **FRS003 Employee Management:** Comprehensive Profile (Personal, Org, Employment, Attachments).
*   **FRS004 Payroll:** Configurable Salary Structure, Auto-calculation, Payslips, Bank Transfer.
*   **FRS005 Leave:** Dashboard, Application Workflow, Balance Tracking.
*   **FRS006 Attendance:** Biometric Sync, Daily Logs, Reports.
*   **FRS007 Expense:** Claim Submission, Approval, Categorization.
*   **FRS008 Policy:** Holiday Calendar, Salary Rules.
*   **FRS009 Notice Board:** Create/View Notices with targeting.
*   **FRS010 User Management:** CRUD Users, Role Assignment.
*   **FRS011 Reports:** Consolidated reports for all modules (PDF/Excel).

---
*End of existing SRS v1.0 text.*

---

## New Requirements Paste (1.5 Assumptions)
*Pasted from chat on 2025-12-16*

**1.5 Assumptions**
The functional requirements and use cases defined in this document are based upon the following assumptions:

| Ref # | Assumption | Impact |
| :--- | :--- | :--- |
| **US_ASM_001** | **Resources:**<br>• End users will be available to test during the time they agreed to<br>• Training environment will be available in the cloud and offline as needed | Handover, go live and final signoff |
| **US_ASM_002** | **Delivery:**<br>• Project environment fully configured and available as expected<br>• Test cases created, training environment configured | Handover, go live and final signoff |
| **US_ASM_003** | **Budget:**<br>• Project costs will stay the same<br>• Training conducted internally (no extra cost) | Project budget |
| **US_ASM_004** | **Finances:**<br>• Funding available when needed | Implementation |
| **US_ASM_005** | **Scope:**<br>• Scope will not change after signoff | Project scope |
| **US_ASM_006** | **Schedule:**<br>• Tools available as planned<br>• Offshore contracts executed within 2 weeks | Project completion |
| **US_ASM_007** | **Methodology:**<br>• Agile Scrum methodology<br>• Team governance guidelines | Project execution |
| **US_ASM_008** | **Technology:**<br>• **MERN Stack** framework<br>• Hosted on **AWS/GCP**<br>• Works on all compatible browsers | Ease of installation/setup |
| **US_ASM_009** | **Architecture:**<br>• REST API architecture<br>• Reside in offsite AWS/GCP cloud | |

---

## New Requirements Paste (1.6 General Constraints)
*Pasted from chat on 2025-12-16*

**1.6 General Constraints**
| Constraint | Impact |
| :--- | :--- |
| **System Admin Limit** | There will be only **one** system admin in the system. |
| **Admin Privileges** | Can create, edit and delete other Admin users. |
| **Delete Operation** | Available **only** to the administrator. No validation check on delete (to reduce complexity). |
| **Data Consistency** | System admin is responsible for data consistency (must be careful before deletion). |

| **Deletion Policy** | Restricted to Admin; **NO Validation** (Hard Delete); Admin responsible for consistency. |

---

## New Requirements Paste (2. Product Functions)
*Pasted from chat on 2025-12-16*

**2. Product Functions**
**2.1 Product Perspective**
*   **Type:** Online web-based ERP solution.
*   **Objective:** Automate HRM, Accounts, Training, Assets, Charity, etc.
*   **Integrations:** SMS, Email, Payment Gateway. (Live Chat in Phase 2).
*   **UI/UX:** Dynamic, responsive, simple, and interactive for novice users.
*   **Scalability:** Integration with third-party portals.

**2.2 Product Functions**
| ID | Function |
| :--- | :--- |
| **#1** | Admin adds user accounts to database. |
| **#2** | Super Admin: Add/Change/Delete users & Role Management. |
| **#3** | HR Manager: Register employees, view profiles, Attendance, Leave adjustment. |
| **#4** | Training Manager: Manage training process [Future Scope]. |
| **#5** | Accounts Manager: Manage assignments, expenses, payroll, accounting [Future Scope]. |
| **#6** | CSS Manager: Manage Charity & Social activities [Future Scope]. |
| **#7** | Procurement: Purchase, damage, supplier management [Future Scope]. |
| **#7** | Procurement: Purchase, damage, supplier management [Future Scope]. |
| **#8** | Integrations: Payment gateway, Instant SMS, Email Notification. |

---

## New Requirements Paste (2.5 User Characteristics)
*Pasted from chat on 2025-12-16*

**2.5 User Characteristics for HRM Module**
| Role | Count | Responsibility / Activity |
| :--- | :--- | :--- |
| **Super Administrator** | 1 | **Administers Portal:** Create/Edit/Delete all users, Role & Permission assignment, Custom Roles.<br>**Config:** Biometric settings, Salary templates, PF rules, Tax settings.<br>**Full Access:** Employees, Payroll, Leave, Attendance, Expense, Policy, Notice, Reports. |
| **HR Administrator** | 1 | **Employee Mgmt:** Add/Edit employees, Upload docs (CV, NID, etc), View Profile.<br>**Operations:** View/Export Attendance, Leave Mgmt, Salary/Payroll Mgmt, Notice Board.<br>**Claims:** Verify and manage expense claims. |
| **HR Manager/Supervisor** | Unknown | **Team Mgmt:** View team list and profiles.<br>**Approvals:** Approve/Reject Leave and Expense claims for direct reports.<br>**Monitoring:** Team attendance summary, Generate team reports. |
| **HR Officer** | Unknown | **Profile:** View/Update own.<br>**Team Support:** View team list/profiles, Attendance details.<br>**Claims:** Add expense claims.<br>**View:** Notices, Reports (as per permission). |
| **Accounts/Finance Officer** | Unknown | **Payroll:** Process monthly salary, Verify calculations, Disburse (Bank/Cash/Cheque), Upload Bank Templates.<br>**Docs:** Generate Payslips (Email), Tax/PF Reports.<br>**Claims:** Review and approve expense claims.<br>**PF:** Manage contributions. |
| **Employee** | Unknown | **Self-Service:** Submit Leave/Expense, View Balance/History, View Attendance %.<br>**Docs:** Download Payslips, Upload Expense proofs.<br>**Info:** View Profile (limited), View Admin Notices, Change Password. |

---

## New Requirements Paste (3.1 User Signup and Login)
*Pasted from chat on 2025-12-16*

**FRS REQ ID:** FRS001
**REQ Title:** Users sign up & login system
**User Story:** As a user I want to sign up in the system and want to login as well.

**Functional Functions:**
*   **Methods:** Google SSO or Email Signup.
*   **Signup Fields:**
    1.  First Name
    2.  Last Name
    3.  Email/Username (Welcome email with login barcode sent after)
    4.  Mobile Phone (OTP Verification)
    5.  Address
    6.  Password
    7.  Re-type Password
    8.  Role (e.g., HR Manager, Staff)
*   **Flow:** Signup -> Verification (OTP) -> Welcome Email -> Basic Setup Page -> User-wise Dashboard.
*   **Constraints:** Email verification / OTP.
*   **Priority:** Essential.

---

## New Requirements Paste (3.1 & 3.2 FRS001/FRS002)
*Pasted from chat on 2025-12-16*

**3. Detailed Functional Requirements**
(Introductory text included in `requirements.md`)

**3.1 User signup and login (FRS001)**
*   **Methods:** Google SSO or Email Signup.
*   **Signup Fields:** First Name, Last Name, Email/Username (Welcome email w/ barcode), Mobile (OTP), Address, Password, Re-type Password, Role (HR Manager/Staff).
*   **Flow:** Signup -> Basic Setup Page -> User-wise Dashboard.
*   **Constraints:** Email verification / OTP.

**3.2 HRM Dashboard Features (FRS002)**
*   **Employee Statistics:** Total, New (current cycle/month), Permanent, Probation. Filters: Day, Month, Date Range.
*   **Attendance Summary:** Total Present, Total Absent. Filters: Day, Month, Date Range.
*   **Leave Summary:** Total Applications. Filters: Day, Month, Date Range.
*   **Calendar:** Read-only (Holidays, Events, Notices).
*   **Note:** Dashboard is user-role specific.

*   **Note:** Dashboard is user-role specific.

---

## New Requirements Paste (3.3 & 3.4 FRS003/FRS004)
*Pasted from chat on 2025-12-16*

**3.3 Employee Management Features (FRS003)**
*   **Data Entry Fields:**
    *   **Basic:** Name, ID (Auto/Manual), Mobile, Email.
    *   **Org:** Institution (As-Sunnah, Madrasatus Sunnah), Branch, Dept, Designation.
    *   **Employment:** Joining Date, Status (Probation/Volunteer/Intern/Permanent), Salary Info, Bank Info.
    *   **Personal:** DOB, Blood Group, NID/Passport, Marital Status.
    *   **Emergency:** Name, Relation, Mobile, Address.
    *   **Address:** Present, Permanent.
    *   **Attachments:** CV, Profile Image.
*   **Employee List:** Filterable (Inst, Branch, Dept, Desig, Status). Columns: Name, ID, Dept, Mobile, Status.
*   **Edit:** Track edit history. Validation on edits.
*   **View Page:** All info + Leave Calendar + "Total Days of Employment" (Auto-calc).
*   **Constraints:** Check Duplicate ID. Secure storage.

**3.4 Payroll Management Module (FRS004)**
*   **Auto-Calculation:** Gross, Basic, House Rent, Medical, Conveyance, PF Deduction.
*   **Configuration:** Accounts Manager sets designation-wise structure.
*   **Payroll List:** Serial, Name, Designation, Salary Breakup, Overtime, Compensation Days, Gross, Absent Days, Tax, PF Amount, Net Salary.
*   **Payment:** Bank (template upload), Cash, Cheque. Auto-generate payment sheets.
*   **Pay Slip:** View Online, Download PDF, Email Auto-send. Shows adjustments/tax/PF.
*   **Salary Certificate:** Customizable format (breakdown, tenure, signature).

*   **Pay Slip:** View Online, Download PDF, Email Auto-send. Shows adjustments/tax/PF.
*   **Salary Certificate:** Customizable format (breakdown, tenure, signature).

---

## New Requirements Paste (3.5 & 3.6 FRS005/FRS006)
*Pasted from chat on 2025-12-16*

**3.5 Leave Management Module (FRS005)**
*   **Leave Dashboard:** Total, Accepted, Rejected, Pending. Filters: Employee, Date, Supervisor, Type. Hierarchy-wise view.
*   **Application Submission:**
    *   **Auto-populate:** Name, ID, Dept, Desig, Supervisor.
    *   **User Input:** Type, Date, Slot, Notes.
    *   **Supervisor View:** Short info (Personal, Leave data, Attendance, Status).
*   **Workflow:** Supervisor Approve/Reject -> HR Override. Validity check on balance. Notifications (SMS/Email/System).
*   **Config:** HR Admin adds leave types.

**3.6 Attendance Tracking and Management Module (FRS006)**
*   **Dashboard:** Insights for HR Admin/Manager.
*   **Biometric Integration:** Daily Sync (In/Out timestamps).
*   **Views:**
    *   **Employee:** Own attendance report only.
    *   **HR/Manager:** View logs for any employee. Filter by Date/Range.
*   **Reports:** Summary/Tracking, Timestamp logs, Absent reports. Excel/PDF Export.

*   **Reports:** Summary/Tracking, Timestamp logs, Absent reports. Excel/PDF Export.

---

## New Requirements Paste (3.7 - 3.11 FRS007-FRS011)
*Pasted from chat on 2025-12-16*

**3.7 Expense Management (FRS007)**
*   **Dashboard:** Expense insights for HR/Admin.
*   **Submission:** Claim category, Amount, Receipt upload (Image/PDF).
*   **Workflow:** Supervisor Approval -> Admin Notification.
*   **Category Mgmt (Admin):** Create/Edit (Bank Charge, Advance, Tax, Conveyance, Purchase), Limits.
*   **Reports:** By Date, Category, Status. Exportable.

**3.8 Policy Management Feature (FRS008)**
*   **Approval:** Policies approved by senior management system.
*   **Calendar:** Admin creates Holiday Calendar (Sync to dashboard/attendance).
*   **Salary Rules:** Define calc rules (%), PF policies, Apply to groups/employees.

**3.9 Notice Board Feature (FRS009)**
*   **Create (HR/Admin):** Title, Description, Attachment, Visibility (Individual/Dept/Branch/All).
*   **Export:** Notice history by date.
*   **View:** Employees see Title, Desc, Attach, Date.

**3.10 User Management Module (FRS010)**
*   **Access:** HR/System Admin edit all info.
*   **Account Mgmt:** Create (Link to Emp ID), Edit (except pass), Activate/Deactivate, Soft Delete. Search (Name, ID, Role, Status).
*   **Roles:** Admin, HR Admin, Supervisor, Employee, Finance, Custom.
*   **Permissions:** Page/Module/Action/Feature level.
*   **Profile (User):** View restricted info (Name, ID, Attendance, Leave). Update Password ONLY (or by Admin).

**3.11 Report Module (FRS011)**
*   **General:** Dynamic filters, Exports (PDF/XLSX/CSV), Scheduled (Optional), Secure Access.
*   **Categories:**
    *   **Employee:** Basic Info, Status, New, Separation, Dept/Branch Distribution.
    *   **Attendance:** Summary, Date Range, History, Late/Early/Absent, Raw Logs.
    *   **Leave:** Summary, Balance, Usage, Dept-wise, Supervisor Response.
    *   **Payroll:** Sheet, Breakdown, Tax, PF, OT, Compensation, Bank Sheet, Disbursement.
    *   **Expense:** Claim, Category-wise, Status, Summary, Date Range.
    *   **Notice:** Dept/Branch Reports.
    *   **User:** User List, Active/Inactive, Login History, Failed Attempts, Password Logs.

---
*End of current text. Add new requirements below.*

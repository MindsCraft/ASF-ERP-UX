# System Requirements Specification (SRS) - ASF ERP

**Version:** 1.0  
**Based on:** ASF ERP HRM Edited SRS (Dec 2025)

## 1. Project Overview & Scope

### 1.1 Long-Term Vision (Future Modules)
The complete ASF ERP system is planned to cover the following modules in future phases:
*   **HRM (Current Phase)**
*   Training Center Management System (TCMS)
*   Accounts Management System (AMS)
*   Asset Management System (AMS)
*   Charity & Social Service (CSS) Project Management
*   Purchase & Procurement System (PMS)

### 1.2 Current Scope: Human Resource Management (HRM)
**Focus:** Automating core HR processes for ASF's multiple institutions and branches.

**In Scope Features:**
*   **Workforce Administration:** Employee master data, hierarchy (roles, branches, departments, institutions).
*   **Time & Attendance:** Biometric login/logout tracking.
*   **Leave Automation:** Approval workflows and balance tracking.
*   **Monthly Payroll:** Salary breakdown, statutory deductions, arrears, tax, and allowances.
*   **Financial Contributions:** Provident Fund (Employer & Employee).
*   **Expense Management:** Claims, reimbursements, category management, and reporting.
*   **Internal Engagement:** Digital notice board, SMS/Email alerts.
*   **Security:** Role-based authentication, unlimited user creation, profile & password management.

### 1.3 Scope Exclusions
The following are explicitly **OUT OF SCOPE** for this phase:
*   **Mobile App Development**
*   **Advanced Data Analytics** (Power BI reporting, ETL Pipeline development)

### 1.4 Project Assumptions & Technical Constraints
*   **Technology Stack (US_ASM_008):**
    *   **Framework:** MERN Stack (MongoDB, Express.js, React, Node.js).
    *   **Architecture:** REST API-based microservices or modular monolith (US_ASM_009).
    *   **Hosting:** Cloud-based (AWS or GCP).
    *   **Browser Compatibility:** Modern browsers (Chrome, Firefox, Edge, Safari).
*   **Key Assumptions:**
    *   **US_ASM_001:** End users available for testing as agreed.
    *   **US_ASM_002:** Training/Test environment fully configured.
    *   **US_ASM_003:** Budget fixed; Training conducted internally.
    *   **US_ASM_005:** Scope locked after signoff.
    *   **US_ASM_007:** Adherence to Agile Scrum methodology.

### 1.5 General Constraints (1.6)
*   **System Admin Limit:** Only **ONE** System Admin account allowed.
*   **Admin Power:** Can Create, Edit, and Delete other Admin users.
*   **Deletion Policy:**
    *   Delete operation restricted to Administrator only.
    *   **NO Validation Check:** Deletion has no constraints to reduce complexity (Hard Delete).
    *   **Responsibility:** System Admin is solely responsible for data consistency.

## 2. Product Functions

### 2.1 Product Perspective
*   **Web-Based ERP:** Online solution to automate HRM, Accounts, Training, Assets, Charity, etc.
*   **Modules:**
    *   **Core:** HRM, Accounts, Training, Asset Management, Charity (CSS), User Management, CRM.
*   **Integrations:**
    *   **Phase 1:** SMS, Email, Payment Gateway.
    *   **Phase 2:** Live Chat.
*   **Scalability:** Designed to integrate with third-party portals.
*   **UX Goals:** High-quality, dynamic, responsive interface; simple for novice users.

### 2.2 Product Functions (High-Level)
| # | Role | Function Description |
| :--- | :--- | :--- |
| **1** | Admin | Add user accounts to application database. |
| **2** | Super Admin | CRUD Users, Role Management. |
| **3** | HR Manager | Register employees, View Profile, Attendance, Leave Balance. |
| **4** | Training Mgr | Manage Training process/activities [Future Scope]. |
| **5** | Accounts Mgr | Manage Income/Expense, Payroll, Accounting [Future Scope/Partial]. |
| **6** | CSS Manager | Charity & Social activities [Future Scope]. |
| **7** | Procurement | Purchase, Damage, Supplier management [Future Scope]. |
| **8** | System | Payment Gateway, SMS, Email Notifications. |

### 2.3 User Characteristics (Detailed)
| Role | Count | Key Responsibility |
| :--- | :--- | :--- |
| **Super Admin** | 1 | **System Config:** Users, Roles, Biometric Settings, Salary Templates, PF Rules. Full Access to all modules. |
| **HR Admin** | 1 | **Operations:** Employee Onboarding, Payroll Processing, Leave Management, Attendance Reports, Notice Board. |
| **HR Manager** | TBD | **Team Lead:** Approve Leave/Expenses for direct reports. Monitor team attendance & performance. |
| **HR Officer** | TBD | **Support:** View team regular profiles/attendance. Assist in claims. |
| **Accounts** | TBD | **Finance:** Payroll Verification, Disbursement (Bank/Cheque), Tax/PF Reports, Claim Payment. |
| **Employee** | TBD | **Self-Service:** Submit Leave/Expenses, View Payslips, Check Attendance, Read Notices. |

## 3. Detailed Functional Requirements (HRM Module)
In this chapter, the functional requirements associated with a feature will be described for the ASF ERP system (HRM). These are the software capabilities that must be present for the user to perform the services provided by the feature.

### 3.1 User signup and login (FRS001)
*   **User Story:** As a user I want to sign up in the system and want to login as well.
*   **Methods:** Google SSO, Email/Password Signup.
*   **Signup Page Data Fields:**
    1.  First Name
    2.  Last Name
    3.  Email/Username (Welcome email with login barcode sent after signup)
    4.  Mobile Phone (OTP verification required)
    5.  Address
    6.  Password
    7.  Re-type Password
    8.  Role (e.g., “HR manager/Staff”)
*   **Post-Login Flow:** Sign-in -> Basic Setup Page -> User-wise Dashboard.
*   **Constraints:** Email verification / OTP is essential.
*   **Employee Database:**
    *   **Basic Info:** Name, ID (Auto/Manual), Contact details.
    *   **Org Details:** Institution, Branch, Department, Designation.
    *   **Employment:** Joining Date, Status (Probation/Permanent/Volunteer/Intern), Salary, Bank Info.
    *   **Personal:** DOB, Blood Group, NID/Passport, Marital Status.
    *   **Emergency Contact:** Name, Relation, Phone, Address.
    *   **Attachments:** CV, Profile Image.
*   **Listing:** Searchable/Filterable list (by Branch, Dept, Status).
*   **Profile View:** Comprehensive view including Auto-calculated "Total Days of Employment".

### 3.2 HRM Dashboard Features (FRS002)
*   **User Story:** Dashboard components must adapt to domain and user expectations.
*   **Employee Statistics:**
    *   Total number of current employees.
    *   Number of new employees added in current cycle (month).
    *   Count of permanent employees.
    *   Count of probation employees.
    *   **Filters:** Day, Month, Date Range.
*   **Attendance Summary:**
    *   Total present employees.
    *   Total absent employees.
    *   **Filters:** Day, Month, Date Range.
*   **Leave Summary:**
    *   Total number of leave applications.
    *   **Filters:** Day, Month, Date Range.
*   **Calendar:** Read-only calendar showing holidays, events, and notices.
*   **User-Specific:** System will display the user-wise specific dashboard based on the user’s role and permission.

### 3.4 Payroll Management Module (FRS004)
*   **User Story:** User performs all payroll management functions and processing.
*   **Salary Structure Automation:**
    *   **Auto-Calculate:** Gross Salary, Basic, House Rent, Medical, Conveyance, Provident Fund deductions.
    *   **Configuration:** Accounts Manager configures designation-wise salary structure.
*   **Payroll List View:**
    *   Columns: Serial, Employee Name, Designation, Salary Breakup (Basic/Rent/Med/Conv), Overtime, Compensation Days, Gross Salary, Absent Days, Tax, PF Amount, Net Salary.
*   **Salary Payment:**
    *   **Methods:** Bank, Cash, Cheque.
    *   **Bank Transfer:** Admin uploads bank-specific templates.
    *   **Output:** System generates payment sheets automatically.
*   **Salary Pay Slip:**
    *   View monthly pay slip online.
    *   Download as PDF.
    *   **Auto-Email:** Sent automatically once processed.
    *   **Content:** Adjustments, allowances, tax, PF, deductions shown clearly.
*   **Salary Certificate:**
    *   HR creates certificate for any employee.
    *   Customizable format (includes salary breakdown, tenure, signature).

### 3.5 Leave Management Module (FRS005)
*   **User Story:** Users perform all leave application and management functions.
*   **Leave Dashboard:**
    *   **Metrics:** Total Applications, Accepted, Rejected, Pending.
    *   **Filters:** Employee, Date, Supervisor, Leave Type.
    *   **Hierarchy:** Supervisors view applications hierarchy-wise.
*   **Leave Application Submission:**
    *   **Auto-Populated Fields:** Name, ID, Department, Designation, Supervisor details.
    *   **User Input:** Leave Type, Date, Slot, Notes.
    *   **Supervisor View:** Sees applicant's Personal details, Leave data, Attendance data, Employment status.
*   **Approval Workflow:**
    *   Supervisor approves/rejects -> HR Override capability.
    *   System updates balance automatically.
    *   **Validation:** System checks balance before submission.
    *   **Notifications:** SMS/Email/System alerts for all actions.
*   **Configuration:** HR Admin manages leave types/categories.

### 3.6 Attendance Tracking and Management Module (FRS006)
*   **User Story:** Users perform all attendance tracking and management functions.
*   **Attendance Dashboard:**
    *   Insights for HR Admin/Manager (Late/Absent/Present).
*   **Biometric Integration:**
    *   System tracks Biometrics/In-Out of employees.
    *   **Sync:** Daily sync of login/logout timestamps from devices.
*   **Attendance View:**
    *   **Employee:** View ONLY own attendance report.
    *   **HR Admin/Manager:** View logs for ANY employee. Filter by Date or Date Range.
*   **Attendance Reports:**
    *   Employee-wise Summary/Tracking reports.
    *   Detailed timestamp logs.
    *   Employee-wise Absent reports.
    *   **Export:** Excel/PDF formats supported.

### 3.7 Expense Management (FRS007)
*   **Use Case:** Users perform all expense management functions.
*   **Dashboard:** Expense monitoring dashboard with insights for HR Admin/Manager.
*   **Claim Submission:**
    *   **Actions:** Create claim, Select Category, Enter Amount.
    *   **Attachments:** Upload images/PDF receipts.
*   **Approval Workflow:**
    *   Route to Supervisor for approval.
    *   Notify Admin after approval.
*   **Claim Category Management (Admin):**
    *   **Actions:** Create, Edit names, Set limits.
    *   **Predefined Categories:** Bank Charge, Advance, Cash, Company Tax, Conveyance, Purchase.
*   **Reports:**
    *   Filter by Date range, Category, Status (Pending/Approved/Rejected).
    *   **Export:** Excel, Word, PDF.

### 3.8 Policy Management Feature (FRS008)
*   **Use Case:** Users perform all policy management functions.
*   **Governance:** Organization policies configured in system; must be approved by senior management via system.
*   **Calendar Management:**
    *   **Admin/HR:** Create details, Add/Edit/Delete holiday dates.
    *   **Sync:** Holidays sync to employee dashboards & attendance calculators.
*   **Salary Structure Rules:**
    *   **HR/Accounts:** Define calculation rules.
    *   **Configuration:** Percentages for Basic, House Rent, Medical, etc.
    *   **Policies:** Set PF contribution policies.
    *   **Scope:** Apply rules across all employees or specific groups.

### 3.9 Notice Board Feature (FRS009)
*   **Use Case:** Users perform all notice board functions.
*   **Governance:** Notices must be approved by senior management (system feature).
*   **Create Notice (HR Admin/Manager):**
    *   **Fields:** Title, Description, Attachments.
    *   **Visibility:** Individual, Department, Branch, or All Employees.
    *   **Export:** Export notices by date range.
*   **View Notices (All Employees):**
    *   See Title, Description, Attachments, Published Date.

### 3.10 User Management Module (FRS010)
*   **User Story:** User manages all system users.
*   **Admin Access:** HR Admin/System Admin can edit all user info.
*   **User Account Management:**
    *   **Create:** Name, Email, Mobile, Employee ID (Link to Employee Module), Role, Status.
    *   **Edit:** All details except password.
    *   **Actions:** Activate/Deactivate, Soft Delete (inactive users cannot log in).
    *   **Search/Filter:** Name, Employee ID, Role, Status.
*   **Role Management:**
    *   **Predefined:** Admin, HR Admin, Supervisor, Employee, Finance/Payroll.
    *   **Custom:** Created by Admin.
    *   **Capabilities:** Granular permission sets (e.g., Approve Claims, Edit Policies, View Payroll).
*   **Permission Control:**
    *   **Levels:** Page, Module, Action (CRUD), Feature (e.g., View Salary breakdown).
*   **User Profile Management:**
    *   **View:** Image, Name, ID, Email, Mobile, Attendance %, Leave Status, Employment Status.
    *   **Update:** Password ONLY (or updated by HR Admin).

### 3.11 Report Module (FRS011)
*   **User Story:** Admin/HR/Accounts export customized reports.
*   **General Features:**
    *   Consolidated reporting for all modules.
    *   **Dynamic Filters:** Dept, Branch, Employee, Date Range.
    *   **Exports:** PDF, Excel (XLSX), CSV.
    *   **Security:** Access based on user role permissions.
*   **Report Categories:**
    *   **Employee:** Basic Info, Status (Probation/Permanent), New Hires, Separation (Inactive), Distribution (Dept/Branch).
    *   **Attendance:** Daily Summary, Date Range, History, Late Entry, Early Exit, Absent, Monthly Summary, Raw Biometric Logs.
    *   **Leave:** Application Summary (Status-wise), Balance, Type Usage (Medical/Casual/etc), Dept-wise, Supervisor Response Time.
    *   **Payroll:** Monthly Sheet, Breakdown, Tax Deduction, PF Contribution, Overtime, Compensation Workday, Bank Payment Sheet (Template), Disbursement Status.
    *   **Expense:** Claim Report, Category-wise, Status Report, Employee Summary, Date Range Analytics.
    *   **Notice:** Dept/Branch Notice Report.
    *   **User Mgmt:** User List, Active/Inactive, Login History, Failed Attempts, Password Logs.





# Master Information Architecture & Sitemap
**Status:** Canonical Reference
**Alignment:** 100% Sync with SRS (FRS001 - FRS011)

This document serves as the absolute blueprint for the application. Every screen listed here maps directly to a Functional Requirement Specification (FRS).

---

## 1. System Navigation (Sidebar)
**Ordering:** Strictly sequential based on SRS.

| Ref ID | Module | Navigation Label | Access |
| :--- | :--- | :--- | :--- |
| **FRS002** | HRM Dashboard | **Dashboard** | All |
| **FRS003** | Employee Mgmt | **Employees** | Admin/Manager |
| **FRS004** | Payroll Mgmt | **Payroll** | Finance/Admin |
| **FRS005** | Leave Mgmt | **Leave** | All |
| **FRS006** | Attendance | **Attendance** | All |
| **FRS007** | Expense Mgmt | **Expense** | All |
| **FRS008** | Policy Mgmt | **Policies** | Admin |
| **FRS009** | Notice Board | **Notices** | All |
| **FRS010** | User Mgmt | **Users** | Super Admin |
| **FRS011** | Reporting | **Reports** | Admin/Finance |

---

## 2. Screen-by-Screen Specification

### 3.1 User Signup & Login (FRS001)
**Scope:** Public Access (No Sidebar).

*   **Screen 1.0: Login Page**
    *   **Input:** Email/Username, Password.
    *   **Actions:** Sign In, Continue with Google, Forgot Password, Sign Up (Toggle).
*   **Screen 1.1: Signup Page**
    *   **Input:** First Name, Last Name, Email, Mobile, Address, Password, Confirm Password, Role Request.
    *   **Process:** triggers Admin Approval workflow.

### 3.2 HRM Dashboard (FRS002)
*   **Screen 2.0: Admin Dashboard**
    *   **Stats Cards:** Total Employees, New Hires, Permanent, Probation.
    *   **Widgets:** Attendance (Pie Chart), Pending Leaves (List), Notices (List).
    *   **Filters:** Day, Month, Date Range.

### 3.3 Employee Management (FRS003)
*   **Screen 3.0: All Employees (Grid)**
    *   **Columns:** Name, ID, Dept, Branch, Mobile, Status.
    *   **Filters:** Institution, Branch, Dept, Status.
*   **Screen 3.1: Add Employee (Wizard)**
    *   **Step 1 Basic:** Name, ID, Mobile, Email.
    *   **Step 2 Org:** Institution, Branch, Dept, Designation.
    *   **Step 3 Emp:** Join Date, Status, Salary, Bank Info.
    *   **Step 4 Personal:** DOB, Blood Grp, NID, Marital.
    *   **Step 5:** Emergency Contact, Address.
    *   **Step 6:** Attachments (CV, Image).
*   **Screen 3.2: Employee Profile**
    *   **Tabs:** Overview (Stats), Personal, Job, Documents.

### 3.4 Payroll Management (FRS004)
*   **Screen 4.0: Monthly Salary Sheet**
    *   **Grid:** Name, Designation, Basic, Rent, Medical, Conv, OT, Absent Deduction, Tax, PF, **Net Pay**.
    *   **Actions:** Process, Export Bank Template.
*   **Screen 4.1: Payslip View**
    *   **Layout:** Earnings vs Deductions.
    *   **Actions:** Download PDF, Email.

### 3.5 Leave Management (FRS005)
*   **Screen 5.0: Leave Dashboard**
    *   **Metrics:** Total, Accepted, Rejected, Pending.
*   **Screen 5.1: Apply Modal**
    *   **Inputs:** Type, Start Date, End Date, Reason.
    *   **Logic:** Auto-calc days, Supervisor routing.
*   **Screen 5.2: Approval Queue**
    *   **List:** Pending requests with "Approve/Reject" buttons.

### 3.6 Attendance Tracking (FRS006)
*   **Screen 6.0: Daily Log (Admin)**
    *   **Grid:** Name, Date, In-Time, Out-Time, Status.
    *   **Integration:** Synced with Biometric.
*   **Screen 6.1: My Attendance**
    *   **View:** Calendar showing own Present/Absent status.

### 3.7 Expense Management (FRS007)
*   **Screen 7.0: My Claims**
    *   **Form:** Category (Travel/Food), Amount, Attachment (Receipt).
*   **Screen 7.1: Claim Manager**
    *   **List:** Pending approvals.
    *   **Config:** Set Category Limits.

### 3.8 Policy Management (FRS008)
*   **Screen 8.0: Holiday Calendar**
    *   **Actions:** Add/Edit Holidays.
*   **Screen 8.1: Salary Rules**
    *   **Inputs:** % setup for House Rent, Medical, PF.

### 3.9 Notice Board (FRS009)
*   **Screen 9.0: Notice Feed**
    *   **List:** Title, Date, Download.
*   **Screen 9.1: Create Notice**
    *   **Inputs:** Title, Body, Attachment, Target (Branch/Dept).

### 3.10 User Management (FRS010)
*   **Screen 10.0: User Directory**
    *   **Grid:** Name, Role, Employee Link, Status.
    *   **Actions:** Activate/Deactivate, Soft Delete.
*   **Screen 10.1: Permission Matrix**
    *   **Grid:** Roles vs Modules (Checkboxes).

### 3.11 Reports (FRS011)
*   **Screen 11.0: Report Generator**
    *   **Input:** Select Module, Select Date Range, Select Output Format (PDF/Excel).

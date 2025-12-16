# Information Architecture & Sitemap
**Project:** ASF ERP - HRM Module
**Version:** 1.0

## 1. High-Level Navigation Structure
The application will use a **Sidebar Navigation** layout. The menu items will dynamically toggle based on the logged-in user's role.

### 1.1 Core Menu Items (Top Level)
1.  **Dashboard**
2.  **Employee Management**
3.  **Attendance**
4.  **Leave Management**
5.  **Payroll**
6.  **Expense**
7.  **Notice Board**
8.  **Reports**
9.  **User Management** (Admin Only)
10. **Settings / Configuration** (Admin Only)

---

## 2. Detailed Sitemap

### 2.1 Dashboard
*   **Overview:** Key metrics (Employee count, Attendance summary, Pending actions).
*   **Widgets:**
    *   Attendance Today (Present/Absent/Late).
    *   Leave Requests (Pending Approval).
    *   Notice Board (Latest 5).
    *   My Stats (For Employee: Leave Balance, Attendance %).

### 2.2 Employee Management
*   **All Employees:** Searchable list table.
*   **Add Employee:** Multi-step form (Basic, Employment, Personal, Bank).
*   **Employee Profile:** (Tabs: Overview, Personal, Job, Documents, Salary).
*   **Designation Hierarchy:** Tree view of org structure (Optional).

### 2.3 Attendance
*   **My Attendance:** Calendar view of own logs.
*   **Daily Log:** Admin view of all employee scans today.
*   **Monthly Report:** Grid view of attendance status (P/A/L) for the whole month.
*   **Manual Entry:** Form to fix missing punches (Admin/Manager only).

### 2.4 Leave Management
*   **My Leaves:**
    *   **Apply for Leave:** Form (Type, Date, Reason).
    *   **Leave History:** List of past applications with status.
    *   **Leave Balance:** Cards showing Available/Used days.
*   **Leave Requests (Manager/Admin):**
    *   **Pending Approval:** Queue of requests to approve/reject.
    *   **All Applications:** Historical log of team's leaves.
*   **Leave Calendar:** Company-wide or Team-wide holiday/leave view.

### 2.5 Payroll
*   **Salary Sheet:** Generated monthly payroll list.
*   **Pay Slips:** Individual view to download PDF.
*   **Salary Certificate:** Request/Generate form.
*   **Tax & PF:** Summary reports of deductions.

### 2.6 Expense
*   **My Claims:** List of own expenses + "New Claim" button.
*   **Process Claims (Manager):** Approval queue.
*   **History:** Archive of paid claims.

### 2.7 Notice Board
*   **All Notices:** List view of active notices.
*   **Create Notice:** Form with audience selector and attachment upload.

### 2.8 Reports
*   **Employee Reports:** (Joiners, Leavers, Status).
*   **Attendance Reports:** (Absenteeism, Late Arrivals).
*   **Financial Reports:** (Payroll summary, Expense summary).

### 2.9 User Management (Admin)
*   **Users:** List of system logins.
*   **Roles & Permissions:** Matrix to toggle feature access.

### 2.10 Settings
*   **General:** Organization info, Logo.
*   **Biometric Config:** API keys, Device IPs.
*   **Leave Types:** Manage categories (Sick, Casual).
*   **Salary Rules:** Allowances, Deductions setup.
*   **Holidays:** Calendar configuration.

---

## 3. Role-Based View Matrix

| Feature | Super Admin | HR Admin | Manager | Employee |
| :--- | :---: | :---: | :---: | :---: |
| **Dashboard** | Full Org Stats | Full Ops Stats | Team Stats | Personal Stats |
| **Employee** | Create/Edit/Delete | Create/Edit | Read (Team) | Read (Self) |
| **Attendance** | Full Access | Full Access | View Team | View Self |
| **Leave** | Override | Approve/Manage | Approve Team | Apply |
| **Payroll** | Config/Process | Process | View Team | View Slip |
| **User Mgmt** | Full Access | Full Access | - | - |
| **Settings** | Full Access | Limited | - | - |

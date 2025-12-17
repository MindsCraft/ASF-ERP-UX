# Wireframe W10: User Management
**Requirement ID:** FRS010
**Role:** Super Admin

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 10.0: User Directory
**Goal:** Control system access and user lifecycle management.

**Filter Bar:** 
*   Role (All/Super Admin/HR Admin/Manager/Employee/Custom)
*   Status (Active/Inactive/Suspended)
*   Department, Branch (for filtering by organization)
*   Last Login (Recent/This Week/This Month/Inactive)

**Grid Columns:**
1.  **User Name** (Avatar + Name, linked to Employee Profile)
2.  **Employee ID** (Linked to Employee Module - FRS010 requirement)
3.  **Email / Username**
4.  **Assigned Role** (Pill with role color coding)
5.  **Department/Branch** (From linked employee data)
6.  **Last Login** (Timestamp with relative time)
7.  **Status** (Toggle: Active/Inactive with visual indicator)
8.  **Actions:** [View Profile] [Edit User] [Reset Password] [Edit Permissions] [View History] [Soft Delete]

**Bulk Actions:**
*   Select multiple users for bulk role assignment
*   Bulk activate/deactivate users
*   Bulk password reset with email notifications

### 1.5 Employee Linking (FRS010 Requirement)
**Goal:** Connect user accounts to employee profiles.

**User Creation Process:**
1.  **Select Employee:** Dropdown of employees without user accounts
2.  **Auto-populate:** Name, email, department from employee data
3.  **Set Credentials:** Username, temporary password, role assignment
4.  **Link Validation:** Ensure one-to-one mapping between user and employee

## 2. Screen 10.1: Role & Permissions Matrix
**Goal:** Granular security and custom role creation (FRS010 requirement).

**Predefined Roles:**
*   Super Admin, HR Admin, HR Manager, HR Officer, Accounts, Employee

**Custom Role Creation (FRS010 Requirement):**
*   **Role Name:** Text input for custom role names
*   **Role Description:** Text area describing role purpose
*   **Copy From:** Dropdown to copy permissions from existing role
*   **Actions:** [Create Role] [Edit Role] [Delete Role] [Duplicate Role]

**Permission Matrix Layout:**
*   **Rows:** Modules (Employee, Payroll, Leave, Attendance, Expense, Policy, Notice, User Management, Reports)
*   **Columns:** Permission Types (View, Create, Edit, Delete, Approve, Export)
*   **Cells:** Checkboxes for granular permission control
*   **Advanced Permissions:** 
    *   View Salary Details (Yes/No)
    *   Approve Claims (Yes/No)  
    *   Edit Policies (Yes/No)
    *   Generate Reports (Yes/No)

### 2.2 User Activity Tracking (FRS010 Requirement)
**Goal:** Monitor user system activity and security.

**Login History:**
*   **Columns:** User, Login Time, IP Address, Device, Status (Success/Failed)
*   **Failed Attempts:** Track and alert on multiple failed logins
*   **Session Management:** Active sessions with logout capability
*   **Export:** Login history reports in Excel/PDF

**Password Management:**
*   **Password Logs:** Track password change history with timestamps
*   **Password Policy:** Enforce complexity requirements
*   **Reset Tracking:** Log password reset requests and completions
*   **Security Alerts:** Notify admins of suspicious activities

## 3. SRS Alignment Check
*   ✅ **Custom Roles:** Admin can create custom roles with granular permissions (FRS010 requirement).
*   ✅ **Employee Linking:** User accounts linked to Employee Module with ID reference (FRS010 requirement).
*   ✅ **Soft Delete:** Status toggle for user deactivation without data loss.
*   ✅ **Login History:** Complete tracking of login attempts, failures, and session management.
*   ✅ **Password Logs:** Track password changes and reset activities (FRS010 requirement).
*   ✅ **Permission Control:** Page, Module, Action, and Feature-level permissions.
*   ✅ **Security:** Failed login tracking and suspicious activity alerts.
*   ✅ **Bulk Operations:** Efficient user management with bulk actions.

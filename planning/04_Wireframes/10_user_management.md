# Wireframe W10: User Management
**Requirement ID:** FRS010
**Role:** Super Admin

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 10.0: User Directory
**Goal:** Control system access.

**Filter Bar:** Role (Admin/HR/Staff), Status (Active/Suspended).
**Grid Columns:**
1.  **User Name** (Linked to Employee ID).
2.  **Email / Username**.
3.  **Assigned Role** (Pill).
4.  **Last Login** (Timestamp).
5.  **Status** (Toggle: Active/Inactive).
6.  **Actions:** [Reset Password] [Edit Permissions] [Soft Delete].

## 2. Screen 10.1: Role & Permissions Matrix
**Goal:** Granular security (FRS010.4).

**Layout:** Grid.
*   **Rows:** Modules (Payroll, Leave, Expense, etc.).
*   **Columns:** Roles (HR Admin, Manager, Finance, Staff).
*   **Cells:** Checkboxes (Read / Write / Delete).

## 3. SRS Alignment Check
*   ✅ **Soft Delete:** "Status Toggle" implements FRS010.3.
*   ✅ **Link:** User stores "Employee ID" reference (FRS010.3.a).

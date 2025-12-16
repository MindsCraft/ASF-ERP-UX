# Wireframe: Employee Profile Page
**Type:** Low-Fidelity Structure
**Role:** HR Admin / Manager / Employee (Self-View)

![Employee Profile Wireframe](../assets/wireframe_employee_profile.png)

## 1. Layout Zones

### 1.1 Top Header (Navigation & Actions)
*   **Left:** "Back to List" button (Breadcrumb).
*   **Center:** Page Title ("Employee Profile").
*   **Right:**
    *   **Edit Profile:** Button to enable field editing.
    *   **More Actions:** Dropdown (Deactivate User, Print Profile, reset Password).

### 1.2 Left Sidebar (Sticky Identity Column)
*   **Profile Image:** Large circular avatar.
*   **Primary Identity:** Name, Designation, Employee ID.
*   **Status Badge:** "Active" / "Probation" / "On Leave".
*   **Contact Info:** Email, Mobile, Emergency Contact.
*   **Actions:** "Download Resume" (PDF), "View Contract".

### 1.3 Main Content Area (Tabbed Interface)
The visible content changes based on the selected tab in the top navigation bar of this section.

**Tabs:**
1.  **Overview (Default):**
    *   **Key Stats:** Joining Date, Department, Manager (Clickable).
    *   **Timeline:** Vertical activity stream (Recent leave, role change, etc.).
2.  **Personal:** Full DOB, Address, NID/Passport details, Marital status.
3.  **Job:** Branch, Designation history, Salary Grade, Work Shift.
4.  **Documents:** Grid view of uploaded files (CV, Certificates, NID scan).
5.  **Payroll:** Bank Info, Tax settings, Provident Fund status.
6.  **Attendance:** Monthly calendar view of punches.

## 2. Interaction Notes
*   **Edit Mode:** Clicking "Edit" turns text fields into inputs on the current visible tab.
*   **Smart Buttons:** (Inspired by Odoo) Small badges at the top right of the content area showing "12 Leave Days Left", "3 Active Loans".
*   **Responsiveness:** On mobile, tabs become a horizontally scrollable bar or a dropdown menu.

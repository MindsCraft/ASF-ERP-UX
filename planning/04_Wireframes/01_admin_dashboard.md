# Wireframe: HR Admin Dashboard
**Type:** Low-Fidelity Structure
**Role:** Super Admin / HR Admin

![Admin Dashboard Wireframe](../assets/wireframe_admin_dashboard.png)

## 1. Layout Zones

### 1.1 Sidebar Navigation (Left)
*   **Dimensions:** Fixed width (250px).
*   **Menu Items:**
    *   Dashboard (Active State)
    *   Employee Management
    *   Attendance
    *   Leave Requests
    *   Payroll
    *   Expenses
    *   Reports
    *   Settings

### 1.2 Top Header
*   **Search Bar:** Global search ("Type to search employee or action...").
*   **Actions:**
    *   Notification Bell (with badge count).
    *   User Profile Dropdown (Avatar + Name).

### 1.3 Main Content Area (Grid System)

**Row 1: Key Metrics (4 Cards)**
*   **Total Employees:** Count + Trend indicator (e.g., "+3 this month").
*   **Attendance Today:** "% Present" + Circular Progress bar.
*   **Leave Requests:** Count of "Pending" requests.
*   **Expenses:** Total claimed amount pending approval.

**Row 2: Operational View (Split 2:1)**
*   **Left (Large):** Monthly Attendance Graph (Bar chart showing Present/Absent trends).
*   **Right (Sidebar):** "Pending Actions" List (Checklist style).
    *   Items: "John Doe - Sick Leave", "Sarah - Expense Claim".
    *   Action: Click to open Quick View modal.

**Row 3: Quick Access (Grid)**
*   **Add Employee:** Primary Action Button (Large).
*   **Run Payroll:** Shortcut to payroll wizard.
*   **Post Notice:** Shortcut to create new notice.

## 2. Interaction Notes
*   **Hover States:** Cards should lift slightly on hover.
*   **Responsiveness:** On tablet, Sidebar collapses to Icon-only mode.
*   **Click Action:** Clicking a "Pending Request" opens a **Slide-over Drawer** (not a full page load) to keep context.

# Wireframe W06: Attendance Tracking
**Requirement ID:** FRS006
**Role:** All Users (View) / Admin (Manage)

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 6.0: Daily Attendance Log (Admin View)
**Goal:** Monitor workforce presence in real-time.

**Layout:**
*   **Header:** "Daily Attendance - [Today's Date]"
*   **Filter Bar:** Department, Branch, Status (Late/Absent).

**Data Grid (Real-Time Sync):**
| Employee | In-Time | Out-Time | Duration | Status | Logs |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **[Avatar] Name** | 09:02 AM | 06:15 PM | 9h 13m | **Present** | [View Raw] |
| **[Avatar] Name** | 09:45 AM | - | - | **Late** | [Adjust] |
| **[Avatar] Name** | - | - | - | **Absent** | [Mark Leave] |

**Actions:**
*   **Manual Adjustment:** Click row -> Opens "Time Correction" Modal.
*   **Manual Entry:** [Add Manual Entry] button for non-biometric attendance.
*   **Export Reports:** [Export] dropdown (Excel/PDF) - FRS006 requirement.
*   **Bulk Actions:** Select multiple rows for bulk status updates.

### 1.5 Manual Entry Modal (Admin Only)
**Goal:** Record attendance for employees without biometric access.

**Form Fields:**
*   **Employee:** Dropdown with search
*   **Date:** Date picker (cannot be future date)
*   **Check-in Time:** Time picker
*   **Check-out Time:** Time picker (optional)
*   **Status:** Dropdown (Present/Late/Half Day)
*   **Reason:** Text area (for manual entry justification)
*   **Source:** Auto-filled as "Manual Entry"

**Validation:**
*   Check-out must be after check-in
*   Cannot override existing biometric data without admin approval
*   Requires reason for manual entry

## 2. Screen 6.1: My Attendance (Employee View)
**Goal:** Self-monitoring and attendance summary.

**Visual:** Calendar Widget.
*   **Legend:** Green (Present), Red (Absent), Yellow (Leave), Gray (Holiday).
*   **Interaction:** Click a date to see "In/Out" timestamps.
*   **Stats Sidebar:**
    *   "On-Time Arrival: 95%"
    *   "Average Work Hours: 8.5"
    *   "Total Present Days: 22/30"
    *   "Late Arrivals: 3"

### 2.2 Attendance Reports (FRS006 Requirement)
**Goal:** Generate detailed attendance reports.

**Report Types:**
*   **Employee-wise Summary:** Monthly/quarterly attendance percentage
*   **Detailed Timestamp Logs:** Raw biometric data with in/out times
*   **Late Entry Report:** Employees with late arrivals
*   **Early Exit Report:** Employees leaving before scheduled time
*   **Absent Report:** Daily/monthly absence tracking
*   **Monthly Summary:** Department-wise attendance statistics

**Export Options:**
*   **Excel:** Detailed spreadsheet with formulas and charts
*   **PDF:** Formatted report with company letterhead
*   **Filters:** Date range, department, branch, employee status

## 3. SRS Alignment Check
*   ✅ **Biometric Integration:** Daily sync of login/logout timestamps from devices.
*   ✅ **Manual Entry:** Admin can add manual attendance entries with justification.
*   ✅ **Reporting:** Complete attendance reports (Summary, Detailed, Late, Absent) with Excel/PDF export.
*   ✅ **Access Control:** Employee sees own data only, HR Admin/Manager sees all employees.
*   ✅ **Dashboard Integration:** Attendance insights for HR Admin/Manager dashboard.
*   ✅ **Filtering:** Date range and employee-specific filtering capabilities.

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

**Action:**
*   **Manual Adjustment:** Click row -> Opens "Time Correction" Modal.

## 2. Screen 6.1: My Attendance (Employee View)
**Goal:** Self-monitoring.

**Visual:** Calendar Widget.
*   **Legend:** Green (Present), Red (Absent), Yellow (Leave), Gray (Holiday).
*   **Interaction:** Click a date to see "In/Out" timestamps.
*   **Stats Sidebar:**
    *   "On-Time Arrival: 95%"
    *   "Average Work Hours: 8.5"

## 3. SRS Alignment Check
*   ✅ **Biometric Sync:** "View Raw Logs" implies device data (FRS006.2).
*   ✅ **Reporting:** Late/Absent status visualization included.
*   ✅ **Access Control:** Employee sees "Own" only (FRS006.3), Admin sees Grid.

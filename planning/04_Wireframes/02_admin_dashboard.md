# Wireframe W02: HRM Admin Dashboard
**Requirement ID:** FRS002
**Role:** HR Administrator / System Admin

*(Visual Placeholder: Image Generation Quota Paused - Will be added later)*

## 1. Visual Layout
**Style:** Dashboard Grid System (Responsive).
**Navigation:** Sidebar (Left) with "Dashboard" active.

## 2. Detailed Technical Specification
This layout strictly implements **FRS002** widgets and data.

### 2.1 Top Row (Key Metrics)
**Goal:** Immediate operational health check.

| Card Title | Data Source | Logic/Filter |
| :--- | :--- | :--- |
| **Total Employees** | Employee DB | Count of `Status = Active` |
| **New Hires** | Employee DB | Count of `Join Date = This Month` |
| **Permanent Staff** | Employee DB | Count of `Status = Permanent` |
| **Probation Staff** | Employee DB | Count of `Status = Probation` |

### 2.2 Middle Row (Activity Widgets)
**Goal:** Managing daily attendance and leave.

**Widget A: Attendance Summary (Pie Chart)**
*   **Visual:** Ring Chart with Legend.
*   **Segments:** `Present` (Green), `Absent` (Red), `Late` (Appears as slice or sub-text).
*   **Filter:** Defaults to `Today`.

**Widget B: Pending Action Items (List)**
*   **Title:** "Leave Requests Pending"
*   **Content:** Top 5 recent requests.
*   **Columns:** Avatar, Name, Leave Type (Sick/Casual), Status Badge.
*   **Action:** Click row -> Opens **Approval Details**.

### 2.3 Bottom Row (Communication)
**Goal:** Awareness of notices and holidays.

**Widget C: Notice Board Preview**
*   **Content:** List of valid Policy/Notice items.
*   **Display:** Icon, Title, Date.
*   **Action:** "View All" -> Go to FRS009.

**Global Filters (Header)**
*   [Date Range Picker]: Controls stats logic (Default: Current Month).
*   [Department Dropdown]: Filter dashboard by team (e.g., "IT Dept").

## 3. SRS Alignment Check
*   ✅ **Stats:** All 4 metric types from FRS002.1 accounted for.
*   ✅ **Charts:** Attendance summary (FRS002.2) included.
*   ✅ **Notices:** Calendar/Notice integration (FRS002.4) included.

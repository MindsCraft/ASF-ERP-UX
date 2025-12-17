# Wireframe W05: Leave Management
**Requirement ID:** FRS005
**Role:** Employee / Supervisor / HR

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 5.0: Leave Dashboard (Employee View)
**Goal:** Track personal status.

**Cards:**
*   **Metric 1:** Total Applications (Count).
*   **Metric 2:** Accepted (Green).
*   **Metric 3:** Rejected (Red).
*   **Metric 4:** Pending (Yellow).

**Chart:**
*   **Type Usage:** Bar chart showing Sick vs Casual vs Earned usage.

## 2. Screen 5.1: Apply for Leave (Modal)
**Goal:** Quick submission.

**Form Fields:**
1.  **Leave Type** (Dropdown: Sick/Casual/Earned).
2.  **Date Selection** (Start Date - End Date).
3.  **Duration** (Auto-calc: e.g., "3 Days").
4.  **Slot** (Radio: Full Day / Half Day).
5.  **Reason** (Text Area).
6.  **Substitute** (Employee Search - Optional).

**Logic:**
*   Submit triggers "Pending" status.
*   Notification sent to Supervisor.

## 3. Screen 5.2: Approval Queue (Manager View)
**Goal:** Process team requests.

**Layout:** Split View (List Left, details Right).
*   **List Item:** Name, Date Range, Type.
*   **Context Panel (Right):**
    *   **Applicant:** [Avatar] Name, Designation.
    *   **Balance Check:** "Sick Leave: 2/14 Remaining".
    *   **Reason:** [User Text].
    *   **Actions:** [Approve] [Reject] [Override (HR Only)].

## 4. SRS Alignment Check
*   ✅ **Hierarchy:** Supervisor routing (FRS005.4) defined.
*   ✅ **Metrics:** Dashboard counts defined.
*   ✅ **Validation:** Balance check logic noted.

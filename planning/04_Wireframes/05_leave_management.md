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
*   **Balance Validation:** System checks available leave balance before submission.
*   **Submit Flow:** 
    1. Validates leave balance
    2. Sets status to "Pending"
    3. Routes to supervisor for approval
    4. **Notifications:** SMS/Email sent to supervisor (FRS005 requirement)
*   **Error Handling:** Shows error if insufficient balance.

## 3. Screen 5.2: Approval Queue (Manager View)
**Goal:** Process team requests.

**Layout:** Split View (List Left, details Right).
*   **List Item:** Name, Date Range, Type, Priority indicator.
*   **Context Panel (Right):**
    *   **Applicant:** [Avatar] Name, Designation, Department.
    *   **Leave Details:** Type, Duration, Dates.
    *   **Balance Check:** "Sick Leave: 2/14 Remaining" (Live data).
    *   **Attendance Data:** Recent attendance summary.
    *   **Employment Status:** Current status and tenure.
    *   **Reason:** [User Text].
    *   **Actions:** 
        *   [Approve] - Triggers SMS/Email notification
        *   [Reject] - Requires rejection reason + notification
        *   [HR Override] - Available only to HR Admin (FRS005 requirement)

### 3.3 Notification System (FRS005 Requirement)
**Goal:** Automated communication for all leave actions.

**Notification Triggers:**
*   **Application Submitted:** SMS/Email to supervisor
*   **Supervisor Approved:** SMS/Email to applicant + HR
*   **Supervisor Rejected:** SMS/Email to applicant with reason
*   **HR Override:** SMS/Email to all parties
*   **Balance Updated:** System notification to applicant

**Notification Channels:**
*   **SMS:** For urgent approvals and rejections
*   **Email:** For detailed information and documentation
*   **System:** In-app notifications and dashboard alerts

## 4. SRS Alignment Check
*   ✅ **Hierarchy:** Supervisor routing with HR override capability implemented.
*   ✅ **Metrics:** Dashboard with Total, Accepted, Rejected, Pending counts.
*   ✅ **Validation:** Balance check before submission and during approval.
*   ✅ **Notifications:** SMS/Email alerts for all workflow actions (FRS005 requirement).
*   ✅ **Auto-Update:** System automatically updates balance after approval.
*   ✅ **Workflow:** Complete approval workflow with supervisor → HR chain.
*   ✅ **Data Context:** Supervisor sees applicant details, attendance, and employment status.

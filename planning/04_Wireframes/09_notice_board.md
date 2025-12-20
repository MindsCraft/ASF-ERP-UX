# Wireframe W09: Notice Board
**Requirement ID:** FRS009
**Role:** All Users (Reader) / HR Admin (Publisher)

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 9.0: Notice Feed (Public View)
**Goal:** Internal communication hub.

**Layout:** Card Stream.
*   **Card:** [Pinned Icon] **"Office Closed for Eid"**
    *   *Published:* 2 Hours ago.
    *   *Body:* Preview text (2 lines).
    *   *Action:* [Read More] -> Expands modal.

## 2. Screen 9.1: Create Notice (Admin View)
**Goal:** Create announcements with approval workflow (FRS009 requirement).

**Form:**
*   **Title:** [Text Input] (Required)
*   **Description:** [Rich Text Editor] with formatting options
*   **Target Audience:**
    *   Radio buttons: All Employees / Specific Branch / Specific Department / Individual Employee
    *   If Specific -> Show [Multi-select Dropdown]
*   **Priority Level:** Dropdown (Low/Medium/High/Urgent)
*   **Attachments:** [File Upload] (PDF/Image/Document) - Multiple files supported
*   **Effective Date:** Date picker (when notice becomes visible)
*   **Expiry Date:** Date picker (when notice auto-hides)
*   **Actions:** 
    *   [Save as Draft] - Save without publishing
    *   [Submit for Approval] - Send to senior management (FRS009 requirement)
    *   [Publish Immediately] - For urgent notices (senior management only)

### 2.2 Notice Approval Workflow (FRS009 Requirement)
**Goal:** Senior management approval before publication.

**Approval Queue (Senior Management View):**
*   **Pending Notices List:** Title, Created by, Target audience, Priority
*   **Notice Preview:** Full content preview with attachments
*   **Approval Actions:**
    *   [Approve] - Publishes notice immediately
    *   [Reject] - Returns to creator with feedback
    *   [Request Changes] - Send back with modification requests
*   **Approval History:** Track who approved/rejected with timestamps

### 2.3 Notice Export & Reporting (FRS009 Requirement)
**Goal:** Export notices by date range for record keeping.

**Export Features:**
*   **Date Range Filter:** Select start and end dates
*   **Target Audience Filter:** Filter by department/branch/all
*   **Status Filter:** Published/Draft/Expired notices
*   **Export Formats:** PDF (formatted report), Excel (data export), Word (document format)
*   **Content Options:** Include/exclude attachments in export

**Notice Analytics:**
*   **Read Statistics:** Track notice view counts by employee
*   **Engagement Metrics:** Download counts for attachments
*   **Department-wise Reports:** Notice distribution by department/branch

## 3. SRS Alignment Check
*   ✅ **Targeting:** Individual, Department, Branch, and All Employees targeting (FRS009).
*   ✅ **Approval Workflow:** Senior management approval required before publication (FRS009 requirement).
*   ✅ **Export Functionality:** Export notices by date range in multiple formats (FRS009 requirement).
*   ✅ **Visibility Control:** Target audience-based visibility logic implemented.
*   ✅ **Attachments:** Multiple file upload support with various formats.
*   ✅ **Priority System:** Notice priority levels for better organization.

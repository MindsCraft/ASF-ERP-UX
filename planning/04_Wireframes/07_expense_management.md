# Wireframe W07: Expense Management
**Requirement ID:** FRS007
**Role:** Employee (Applicant) / Manager (Approver)

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 7.0: My Claims (Employee View)
**Goal:** Reimbursement submission.

**Form: Submit New Claim**
*   **Categories:** Dropdown (Travel / Food / Bank Charge / Purchase).
*   **Amount:** Currency Input.
*   **Date:** Date Picker.
*   **Proof:** File Upload Area (Receipt Image/PDF).
*   **Action:** [Submit Claim].

**History Grid:**
*   Columns: Date, Category, Amount, Status (Pending/Approved).

## 2. Screen 7.1: Claims Manager (Admin View)
**Goal:** Financial oversight and approval workflow.

**Layout:**
*   **Filter:** By Employee, By Status, By Category, By Date Range.
*   **Approval List:**
    *   Row: [Avatar] Name | Category | Amount | Status | [View Proof]
    *   **Actions:** [Approve] [Reject] [Request More Info]
*   **Bulk Actions:** Select multiple claims for batch approval
*   **Export Options:** [Export Excel] [Export PDF] [Export Word] - FRS007 requirement

### 2.2 Category Management (Admin Only)
**Goal:** Configure expense categories and limits (FRS007 requirement).

**Category Configuration:**
*   **Predefined Categories:** Bank Charge, Advance, Cash, Company Tax, Conveyance, Purchase
*   **Custom Categories:** Admin can create new categories
*   **Category Settings:**
    *   Category Name
    *   Monthly Limit per Employee
    *   Approval Level Required (Supervisor/HR/Finance)
    *   Required Documentation (Receipt mandatory/optional)
    *   Active/Inactive status

**Limit Management:**
*   **Individual Limits:** Set per employee based on designation
*   **Department Limits:** Set limits by department
*   **Monthly/Yearly Caps:** Configure time-based spending limits
*   **Auto-Alerts:** Notify when approaching limits

### 2.3 Expense Reports (FRS007 Requirement)
**Goal:** Generate comprehensive expense analytics.

**Report Types:**
*   **Claim Report:** All claims with status and amounts
*   **Category-wise Report:** Spending breakdown by category
*   **Status Report:** Pending/Approved/Rejected analysis
*   **Employee Summary:** Individual spending patterns
*   **Date Range Analytics:** Time-based expense trends

**Export Formats:**
*   **Excel:** Detailed spreadsheet with pivot tables and charts
*   **Word:** Formatted report with executive summary
*   **PDF:** Professional report with company branding

**Filtering Options:**
*   Date range, Category, Status, Employee, Department, Amount range

## 3. SRS Alignment Check
*   ✅ **Categories:** Configurable categories with predefined and custom options (FRS007).
*   ✅ **Limits:** Category-wise spending limits and alerts implemented.
*   ✅ **Workflow:** Supervisor → Admin approval routing with notifications.
*   ✅ **Reports:** Complete reporting with Excel/Word/PDF export (FRS007 requirement).
*   ✅ **Dashboard:** Expense monitoring dashboard for HR Admin/Manager.
*   ✅ **Attachments:** Receipt upload with image/PDF support.

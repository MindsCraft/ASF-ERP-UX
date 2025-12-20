# Wireframe W08: Policy Management
**Requirement ID:** FRS008
**Role:** HR Admin / System Admin

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 8.0: Holiday Calendar Management
**Goal:** Define workdays and organizational calendar (FRS008 requirement).

**View:** Full Calendar (Yearly/Monthly).
*   **Legend:** Weekend (Gray), Public Holiday (Red), Company Event (Blue), Training Day (Green).
*   **Actions:** 
    *   Click Date -> "Mark as Holiday" -> Input Name (e.g., "Victory Day")
    *   [Add Holiday] button for bulk entry
    *   [Import Calendar] for government holiday lists
    *   [Sync to Employee Dashboards] - Auto-sync feature

**Holiday Management:**
*   **Add/Edit/Delete:** Full CRUD operations on holiday dates
*   **Holiday Types:** Public, Company, Department-specific, Branch-specific
*   **Recurring Holidays:** Set annual recurring dates (e.g., Independence Day)
*   **Approval Required:** Senior management approval for calendar changes (FRS008 requirement)

**Calendar Sync:**
*   Auto-sync to all employee dashboards
*   Integration with attendance calculator
*   Leave application validation against holidays

## 2. Screen 8.1: Salary Structure Rules
**Goal:** Configure automated payroll calculation rules (FRS008 requirement).

**Global Configuration Form:**
*   **Rule 1: House Rent:** [Input] % of Basic Salary
*   **Rule 2: Medical Allowance:** [Input] % of Basic Salary  
*   **Rule 3: Conveyance:** [Input] Fixed Amount or % of Basic
*   **Rule 4: Provident Fund:**
    *   Employee Contribution: [Input] % of Basic
    *   Employer Contribution: [Input] % of Basic
*   **Rule 5: Tax Calculation:** Progressive tax brackets configuration
*   **Rule 6: Overtime Rates:** Hourly rates by designation level

**Rule Application Scope:**
*   **Global Rules:** Apply to all employees
*   **Department-Specific:** Different rules for different departments
*   **Designation-Based:** Rules based on job levels
*   **Branch-Specific:** Location-based rule variations

**Approval Workflow (FRS008 Requirement):**
*   **Draft Status:** Rules can be saved as draft
*   **Senior Management Approval:** Required before activation
*   **Effective Date:** Set implementation date for new rules
*   **Version Control:** Track rule changes and history

### 2.2 Organizational Policies (FRS008 Requirement)
**Goal:** Manage company-wide policies with approval workflow.

**Policy Categories:**
*   **HR Policies:** Leave, attendance, disciplinary procedures
*   **Financial Policies:** Expense limits, reimbursement rules
*   **IT Policies:** System access, data security
*   **Operational Policies:** Working hours, dress code, holidays

**Policy Management:**
*   **Create Policy:** Rich text editor with document attachments
*   **Version Control:** Track policy revisions and changes
*   **Approval Workflow:** Senior management approval required (FRS008)
*   **Distribution:** Target specific departments/branches/all employees
*   **Acknowledgment:** Track employee policy acknowledgments
*   **Effective Dates:** Set policy implementation timelines

## 3. SRS Alignment Check
*   ✅ **Calendar Management:** Holiday creation with sync to employee dashboards and attendance.
*   ✅ **Salary Rules:** Comprehensive percentage-based calculation rules for all allowances.
*   ✅ **Approval Workflow:** Senior management approval required for policies (FRS008 requirement).
*   ✅ **Scope Control:** Apply rules globally or to specific groups (departments/branches).
*   ✅ **PF Policies:** Employee and employer contribution configuration.
*   ✅ **Integration:** Rules sync with payroll processing and attendance systems.

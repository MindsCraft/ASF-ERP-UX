# Wireframe W04: Payroll Management
**Requirement ID:** FRS004
**Role:** Finance Officer / Admin

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 4.0: Monthly Salary Sheet (Grid View)
**Goal:** Process and review bulk salaries.

**Layout:**
*   **Header:** "Payroll Processing - [Month Picker] [Year Picker]"
*   **Actions:** [Process Payroll] (Primary), [Export Bank Sheet], [Print Checks].

**Data Grid Columns (FRS004 Explicit):**
| ID | Column Header | Data Type | Notes |
| :--- | :--- | :--- | :--- |
| 1 | **Serial** | Index | |
| 2 | **Employee Name** | Text | |
| 3 | **Designation** | Text | |
| 4 | **Basic Salary** | Currency | Part of Structure |
| 5 | **House Rent** | Currency | Part of Structure |
| 6 | **Medical** | Currency | Part of Structure |
| 7 | **Conveyance** | Currency | Part of Structure |
| 8 | **Overtime** | Helper | Hours/Amt |
| 9 | **Absent Deduction** | Negative | Based on FRS006 |
| 10 | **Tax** | Negative | Regulatory |
| 11 | **PF Amount** | Negative | Provident Fund |
| 12 | **Net Salary** | **Bold** | *Auto-Calculated* |

## 2. Screen 4.1: Individual Payslip
**Goal:** Employee view of their earnings.

**Structure:** A4 Paper Layout (Digital Representation).
*   **Header:** Institution Logo, Address, Payslip Month.
*   **Employee Info:** Name, ID, Dept, Designation, Bank Acc No.
*   **Table Left (Earnings):** Basic, Rent, Medical, Conveyance, Arrears.
*   **Table Right (Deductions):** PF, Tax, Absent, Advance Salary.
*   **Footer:** Signatures (HR Manager, Accounts Officer).
*   **Actions:** [Download PDF], [Email to Self].
*   **Auto-Email:** System automatically emails payslip once processed (FRS004 requirement).

## 2.5 Screen 4.2: Salary Certificate Generator
**Goal:** HR creates salary certificates for employees (FRS004 requirement).

**Form Layout:**
*   **Employee Selection:** Dropdown with search
*   **Certificate Type:** Dropdown (Employment, Salary, Experience)
*   **Salary Details:** Auto-populated from current salary structure
*   **Custom Fields:**
    *   Purpose of certificate
    *   Additional remarks
    *   Effective date
*   **Template Options:** Letterhead selection
*   **Preview:** Live preview of certificate
*   **Actions:** [Generate PDF], [Print], [Email to Employee]

**Certificate Content:**
*   Company letterhead and details
*   Employee information and tenure
*   Salary breakdown (Basic, Allowances, Gross)
*   Official signatures and seal
*   Issue date and validity

## 3. Screen 4.3: Salary Configuration
**Goal:** Setting the rules (FRS004.2).

*   **Designation Selector:** Dropdown (e.g., "Senior Teacher").
*   **Structure Inputs:**
    *   Basic % (Input)
    *   Rent % (Input)
    *   Medical % (Input)
    *   PF Deduction % (Input)

## 4. SRS Alignment Check
*   ✅ **Columns:** All 12 columns from FRS004 payroll list included.
*   ✅ **Outputs:** Bank Transfer & PDF generation actions included.
*   ✅ **Auto-Email:** Payslips automatically emailed once processed.
*   ✅ **Salary Certificate:** HR can create certificates with customizable format.
*   ✅ **Automation:** Salary structure and deduction logic implemented.
*   ✅ **Payment Methods:** Bank, Cash, Cheque options supported.

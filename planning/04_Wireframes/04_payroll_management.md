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

## 3. Screen 4.2: Salary Configuration
**Goal:** Setting the rules (FRS004.2).

*   **Designation Selector:** Dropdown (e.g., "Senior Teacher").
*   **Structure Inputs:**
    *   Basic % (Input)
    *   Rent % (Input)
    *   Medical % (Input)
    *   PF Deduction % (Input)

## 4. SRS Alignment Check
*   ✅ **Columns:** All 11 columns from FRS004.3 included.
*   ✅ **Outputs:** Bank Transfer & PDF generation actions included.
*   ✅ **Automation:** Deduction logic cited.

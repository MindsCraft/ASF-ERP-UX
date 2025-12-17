# Wireframe W08: Policy Management
**Requirement ID:** FRS008
**Role:** HR Admin / System Admin

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 8.0: Holiday Calendar
**Goal:** Define workdays.

**View:** Full Calendar (Yearly/Monthly).
*   **Legend:** Weekend (Gray), Public Holiday (Red), Company Event (Blue).
*   **Action:** Click Date -> "Mark as Holiday" -> Input Name (e.g., "Victory Day").

## 2. Screen 8.1: Salary Rules Engine
**Goal:** Automate payroll logic (FRS008.4).

**Global Configuration Form:**
*   **Rule 1: House Rent:** [Input] % of Basic.
*   **Rule 2: Medical Allowance:** [Input] % of Basic.
*   **Rule 3: Conveyance:** [Input] Fixed Amount.
*   **Rule 4: Provident Fund:**
    *   Employee Contribution: [Input] %
    *   Employer Contribution: [Input] %

## 3. SRS Alignment Check
*   ✅ **Sync:** Calendar affects attendance logic (FRS008.3).
*   ✅ **Formulas:** Percentage inputs match FRS004/008 requirements.

# Wireframe W04: Payroll Management
**Requirement ID:** FRS004
**Role:** Accounts Manager, Finance Officer, Admin, HR

## 1. Screen 4.0: Payroll Dashboard
**Goal:** Overview of payroll status and quick actions.

**Layout:** Dashboard with status cards and action buttons
- **Header:** "Payroll Management - [Current Month Year]"
- **Status Cards:**
  - Total Employees: 147
  - Payroll Status: Draft/Processing/Completed
  - Total Payroll Amount: $45,230
  - Pending Approvals: 3
- **Quick Actions:** [Process This Month], [View History], [Salary Configuration], [Bank Templates]

## 2. Screen 4.1: Monthly Salary Sheet (Grid View)
**Goal:** Process and review bulk salaries with comprehensive data.

**Header Controls:**
- **Period Selector:** [Month Picker] [Year Picker]
- **Filters:** Department, Branch, Employee Status
- **Actions:** [Process Payroll] (Primary), [Generate Payment Sheet], [Export Bank Sheet], [Bulk Actions]

**Data Grid Columns (BRD Compliant):**
| ID | Column Header | Data Type | Notes |
| :--- | :--- | :--- | :--- |
| 1 | **Serial** | Index | Auto-generated |
| 2 | **Employee Name** | Text | Clickable for details |
| 3 | **Designation** | Text | |
| 4 | **Basic Salary** | Currency | From salary structure |
| 5 | **House Rent** | Currency | From salary structure |
| 6 | **Medical** | Currency | From salary structure |
| 7 | **Conveyance** | Currency | From salary structure |
| 8 | **Overtime** | Currency | Hours × Rate |
| 9 | **Compensation Days** | Currency | **Added per BRD** |
| 10 | **Gross Salary** | Currency | **Auto-calculated** |
| 11 | **Absent Days** | Number | From attendance |
| 12 | **Tax** | Currency | Deduction |
| 13 | **PF Amount** | Currency | Provident Fund |
| 14 | **Net Salary** | **Bold Currency** | **Final amount** |

**Grid Features:**
- **Bulk Selection:** Checkboxes for mass actions
- **Inline Editing:** Overtime and compensation adjustments
- **Status Indicators:** Draft/Approved/Processed per employee
- **Sorting & Filtering:** All columns sortable
- **Pagination:** 50 records per page

## 3. Screen 4.2: Individual Payslip
**Goal:** Employee view of their earnings with complete transparency.

**Layout:** A4 Digital Format with professional styling
- **Header Section:**
  - Institution logo and address
  - "SALARY SLIP - [Month Year]"
  - Employee details (Name, ID, Department, Designation, Bank Account)

**Earnings & Deductions Table:**
| **EARNINGS** | **Amount** | **DEDUCTIONS** | **Amount** |
|--------------|------------|----------------|------------|
| Basic Salary | $XXX | Tax Deduction | $XXX |
| House Rent | $XXX | Provident Fund | $XXX |
| Medical Allowance | $XXX | Absent Days | $XXX |
| Conveyance | $XXX | Advance Salary | $XXX |
| Overtime | $XXX | Other Deductions | $XXX |
| Compensation Days | $XXX | | |
| **Gross Salary** | **$XXX** | **Total Deductions** | **$XXX** |

**Summary Section:**
- **Net Salary:** $XXX (Gross - Deductions)
- **Payment Method:** Bank Transfer/Cash/Cheque
- **Payment Date:** DD/MM/YYYY

**Footer:**
- Digital signatures (HR Manager, Accounts Officer)
- Generated timestamp
- **Actions:** [Download PDF], [Email to Self], [Print]

**Auto-Email Feature:** System automatically emails payslip once salary is processed

## 4. Screen 4.3: Salary Certificate Generator
**Goal:** HR creates professional salary certificates for employees.

**Form Layout:**
- **Employee Selection:** Searchable dropdown with employee details
- **Certificate Type:** Radio buttons (Employment, Salary Verification, Experience)
- **Certificate Details:**
  - Purpose of certificate (text input)
  - Effective date (date picker)
  - Additional remarks (textarea)
  - Include salary breakdown (checkbox)

**Salary Information (Auto-populated):**
- Current designation and department
- Joining date and tenure
- Salary breakdown (Basic, Allowances, Gross)
- Employment status

**Template Options:**
- Letterhead selection (dropdown)
- Signature authority selection
- Language preference (English/Arabic)

**Preview Panel:**
- Live preview of certificate
- Company letterhead and formatting
- Official signatures and seal placement

**Actions:** [Generate PDF], [Print], [Email to Employee], [Save Draft]

## 5. Screen 4.4: Payment Sheet Generator
**Goal:** Generate bank-specific payment sheets automatically.

**Configuration Panel:**
- **Payment Period:** Month/Year selector
- **Bank Template:** Dropdown (SBI, HDFC, Custom templates)
- **Payment Method Filter:** Bank/Cash/Cheque
- **Department Filter:** Multi-select
- **Employee Selection:** All/Selected employees

**Payment Sheet Preview:**
- Bank-specific format with required columns
- Employee details, account numbers, amounts
- Total summary and verification checksums
- Bank routing and institutional details

**Export Options:**
- **Excel Format:** Bank-ready spreadsheet
- **CSV Format:** For bank upload systems
- **PDF Format:** For record keeping

**Actions:** [Generate Sheet], [Download], [Send to Bank], [Save Template]

## 6. Screen 4.5: Bank Template Management
**Goal:** Upload and manage bank-specific payment templates.

**Template Library:**
- **Existing Templates:** List of uploaded bank templates
- **Template Details:** Bank name, format, last used date
- **Actions per template:** Edit, Delete, Duplicate, Set as Default

**Upload New Template:**
- **Bank Selection:** Dropdown or custom entry
- **Template File:** Excel/CSV file upload
- **Column Mapping:** Map system fields to bank template columns
- **Validation:** Preview and validate template format

**Column Mapping Interface:**
| **System Field** | **Bank Template Column** | **Required** |
|------------------|--------------------------|--------------|
| Employee Name | Column A | Yes |
| Account Number | Column B | Yes |
| Net Salary | Column C | Yes |
| Bank Code | Column D | No |

**Actions:** [Upload Template], [Test Template], [Save Mapping]

## 7. Screen 4.6: Comprehensive Salary Configuration
**Goal:** Accounts Manager configures designation-wise salary structures.

**Designation Management:**
- **Designation List:** Table showing all designations with current salary ranges
- **Actions:** Add New, Edit, Delete, Bulk Update
- **Search & Filter:** By department, salary range, status

**Salary Structure Configuration:**
**Selected Designation:** Senior Teacher (example)

**Basic Structure Setup:**
| **Component** | **Type** | **Value** | **% of Gross** |
|---------------|----------|-----------|----------------|
| Basic Salary | Fixed/% | $800 | 40% |
| House Rent | Fixed/% | $400 | 20% |
| Medical Allowance | Fixed/% | $200 | 10% |
| Conveyance | Fixed/% | $150 | 7.5% |

**Deduction Configuration:**
| **Deduction** | **Type** | **Rate** | **Applicable** |
|---------------|----------|----------|----------------|
| Provident Fund | % of Basic | 10% | All employees |
| Tax | Slab-based | Variable | Based on income |
| Professional Tax | Fixed | $20 | All employees |

**Advanced Settings:**
- **Overtime Rate:** $15/hour
- **Compensation Day Rate:** Daily salary rate
- **Absent Day Deduction:** Full day/Half day rates
- **Effective Date:** When structure becomes active

**Bulk Operations:**
- **Apply to Multiple Designations:** Checkbox selection
- **Salary Increment:** Percentage-based bulk increase
- **Import from Excel:** Upload salary structures
- **Export Configuration:** Download current structures

**Validation & Preview:**
- **Sample Calculation:** Preview with dummy employee data
- **Impact Analysis:** Show affected employees count
- **Approval Workflow:** Submit for management approval

**Actions:** [Save Configuration], [Apply Changes], [Preview Impact], [Export Structure]

## 8. Interactive Behaviors & User Flows

### 8.1 Payroll Processing Flow
1. **Dashboard → Monthly Salary Sheet** (Screen 4.0 → 4.1)
2. **Review & Adjust** individual salaries if needed
3. **Bulk Actions** for overtime/compensation entries
4. **Generate Payment Sheet** (Screen 4.4) for selected payment method
5. **Process Payroll** → Auto-generate payslips → Auto-email to employees

### 8.2 Payment Method Handling
- **Bank Transfer:** Generate bank-specific payment sheet using templates
- **Cash Payment:** Generate cash disbursement sheet with signatures
- **Cheque Payment:** Generate cheque printing format with details

### 8.3 Approval Workflow
- **Draft State:** Accounts Manager can edit and adjust
- **Pending Approval:** Submitted to Finance Officer/Admin
- **Approved State:** Ready for processing and payment
- **Processed State:** Payslips generated and distributed

### 8.4 Error Handling & Validations
- **Missing Data:** Highlight employees with incomplete salary data
- **Calculation Errors:** Auto-validate all calculations before processing
- **Bank Template Errors:** Validate template format before upload
- **Duplicate Processing:** Prevent double processing for same period

## 9. SRS Alignment Check
- ✅ **Automatic Calculation:** Gross, Basic, House Rent, Medical, Conveyance, PF
- ✅ **Designation-wise Configuration:** Comprehensive salary structure management
- ✅ **Complete Payroll List:** All 14 required columns (added Compensation Days & Gross)
- ✅ **Payment Methods:** Bank, Cash, Cheque with specific handling
- ✅ **Bank Templates:** Upload and manage bank-specific templates
- ✅ **Payment Sheet Generation:** Automated generation with bank formats
- ✅ **Payslip Features:** View online, PDF download, auto-email
- ✅ **Salary Certificate:** Customizable format with all required fields
- ✅ **Role-based Access:** Accounts Manager, HR, Admin permissions

## 10. Technical Considerations

### 10.1 Security & Permissions
- **Accounts Manager:** Full payroll configuration and processing
- **HR:** View payslips, generate certificates, limited editing
- **Admin:** All permissions including system configuration
- **Employees:** View own payslip only

### 10.2 Performance & Scalability
- **Bulk Processing:** Handle 500+ employees efficiently
- **Background Jobs:** Large payroll processing in background
- **Caching:** Cache salary structures for faster calculations
- **Audit Trail:** Log all payroll changes and approvals

### 10.3 Integration Points
- **Attendance System (FRS006):** Auto-fetch absent days
- **Employee Management (FRS003):** Sync employee data
- **Bank APIs:** Direct integration for payment processing
- **Email System:** Automated payslip distribution

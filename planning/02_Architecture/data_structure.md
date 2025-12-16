# Data Structure & Schema Design
**Project:** ASF ERP - HRM Module
**Version:** 1.0
**Database:** MongoDB (MERN Stack)

## 1. Core Collections

### 1.1 Users (`users`)
*Manages authentication and system access (FRS010).*

| Field | Type | Required | Notes |
| :--- | :--- | :--- | :--- |
| `_id` | ObjectId | Yes | Unique System ID |
| `employeeId` | ObjectId (Ref) | Yes | Link to Employee Profile |
| `username` | String | Yes | Unique (Email) |
| `passwordHash` | String | Yes | Encrypted |
| `role` | String | Yes | Enum: ['Super Admin', 'HR Admin', 'Manager', 'Employee', 'Accounts'] |
| `status` | String | Yes | Enum: ['Active', 'Inactive', 'Banned'] |
| `lastLogin` | Date | No | Timestamp |
| `permissions` | Object | No | Custom overrides { module: [read, write] } |

### 1.2 Employees (`employees`)
*The central master data for workforce (FRS003).*

| Field | Type | Required | Notes |
| :--- | :--- | :--- | :--- |
| `_id` | ObjectId | Yes | |
| `employeeID` | String | Yes | Unique Manual/Auto ID (e.g., ASF-2025-001) |
| `firstName` | String | Yes | |
| `lastName` | String | Yes | |
| `email` | String | Yes | Contact Email |
| `phone` | String | Yes | Primary Mobile |
| **Organization** | | | |
| `institution` | String | Yes | Enum: ['ASF', 'Madrasatus Sunnah'] |
| `branch` | String | Yes | |
| `department` | String | Yes | |
| `designation` | String | Yes | |
| `supervisorId` | ObjectId (Ref) | No | Direct Reporting Manager |
| `joiningDate` | Date | Yes | |
| `status` | String | Yes | Enum: ['Probation', 'Permanent', 'Intern', 'Volunteer'] |
| **Personal** | | | |
| `dob` | Date | No | |
| `bloodGroup` | String | No | |
| `nid` | String | No | National ID / Passport |
| `address` | Object | No | { present: '', permanent: '' } |
| **Financial** | | | |
| `salary` | Number | Yes | Gross Monthly Salary |
| `bankInfo` | Object | No | { bankName: '', accountNo: '', branch: '' } |
| **Meta** | | | |
| `profileImage` | String | No | URL |
| `documents` | Array | No | [{ type: 'CV', url: '...' }] |

---

## 2. Operational Collections

### 2.1 Attendance Logs (`attendance_logs`)
*Daily biometric sync data (FRS006).*

| Field | Type | Notes |
| :--- | :--- | :--- |
| `employeeId` | ObjectId | Ref to Employee |
| `date` | Date | ISO Date (YYYY-MM-DD) |
| `checkIn` | Timestamp | First punch |
| `checkOut` | Timestamp | Last punch |
| `status` | String | Enum: ['Present', 'Absent', 'Late', 'Leave'] |
| `lateTime` | Number | Minutes late (Calculated) |
| `source` | String | Enum: ['Biometric', 'Manual', 'Remote'] |

### 2.2 Leave Applications (`leaves`)
*Leave requests and workflow (FRS005).*

| Field | Type | Notes |
| :--- | :--- | :--- |
| `applicantId` | ObjectId | Ref to Employee |
| `supervisorId` | ObjectId | Who needs to approve |
| `type` | String | Enum: ['Sick', 'Casual', 'Annual', 'Unpaid'] |
| `startDate` | Date | |
| `endDate` | Date | |
| `daysCount` | Number | Calculated duration |
| `reason` | String | User notes |
| `status` | String | Enum: ['Pending', 'Approved_Supervisor', 'Approved_HR', 'Rejected'] |
| `workflowLogs` | Array | [{ user: 'Manager', action: 'Approved', time: '...' }] |

### 2.3 Expenses (`expenses`)
*Reimbursement claims (FRS007).*

| Field | Type | Notes |
| :--- | :--- | :--- |
| `claimantId` | ObjectId | Ref to Employee |
| `category` | String | Enum: ['Transport', 'Food', 'Purchase', 'Tax'] |
| `amount` | Number | |
| `date` | Date | Expense date |
| `attachments` | Array | Receipt URLs |
| `status` | String | Enum: ['Pending', 'Approved', 'Paid', 'Rejected'] |
| `approvedBy` | ObjectId | |

### 2.4 Payroll History (`payrolls`)
*Monthly generated salary sheets (FRS004).*

| Field | Type | Notes |
| :--- | :--- | :--- |
| `employeeId` | ObjectId | |
| `month` | String | Format: "YYYY-MM" |
| `generatedDate` | Date | |
| **Earnings** | | |
| `basic` | Number | % of Gross |
| `houseRent` | Number | |
| `medical` | Number | |
| `conveyance` | Number | |
| `overtime` | Number | Calculated amount |
| **Deductions** | | |
| `tax` | Number | |
| `providentFund` | Number | |
| `absentCheck` | Number | Deduction for unexcused absence |
| **Final** | | |
| `netPayable` | Number | (Earnings - Deductions) |
| `paymentStatus` | String | Enum: ['Unpaid', 'Processed', 'Disbursed'] |

---

## 3. Configuration Collections
*   `settings`: Organization details, Logo, Biometric API configs.
*   `leave_types`: Configurable leave categories and yearly quotas.
*   `holidays`: Company calendar dates.
*   `notices`: Notice board posts with 'targetAudience'.

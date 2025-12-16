# User Flows & Process Diagrams
**Project:** ASF ERP - HRM Module
**Version:** 1.0

## 1. Authentication Flow
*How users access the system and get routed based on their role.*

```mermaid
graph TD
    A[Start: Login Page] --> B{Choose Method}
    B -->|Email/Pass| C[Enter Credentials]
    B -->|Google SSO| D[Google Auth Provider]
    
    C --> E{Valid?}
    D --> E
    
    E -->|No| F[Show Error Message]
    E -->|Yes| G[Check User Role]
    
    G -->|Super Admin| H[Admin Dashboard]
    G -->|HR Admin| I[HR Operational Dashboard]
    G -->|Manager| J[Manager Dashboard]
    G -->|Employee| K[Employee Self-Service Dashboard]
    
    H --> L[Show Org Health Stats]
    I --> M[Show Pending Approvals]
    J --> N[Show Team Attendance]
    K --> O[Show My Attendance & Leave Balance]
```

## 2. Leave Application Workflow
*The process of applying for leave and the approval chain.*

```mermaid
sequenceDiagram
    actor Emp as Employee
    participant Sys as ERP System
    actor Sup as Supervisor
    actor HR as HR Admin

    Emp->>Sys: Click "Apply Leave"
    Sys->>Sys: Check Leave Balance
    alt Insufficient Balance
        Sys-->>Emp: Error "Insufficient Balance"
    else Sufficient Balance
        Emp->>Sys: Submit Form (Date, Reason)
        Sys->>Sup: Send Notification (Email/SMS)
        
        Sup->>Sys: Review Request
        alt Rejected
            Sup-->>Sys: Click Reject
            Sys-->>Emp: Notify "Rejection"
        else Approved
            Sup-->>Sys: Click Approve
            Sys->>HR: Notify "Supervisor Approved"
            
            HR->>Sys: Final Review
            HR-->>Sys: Click Final Approve
            Sys->>Sys: Deduct Leave Balance
            Sys-->>Emp: Notify "Leave Approved"
        end
    end
```

## 3. Payroll Processing Flow
*Monthly salary generation cycle by Accounts/HR.*

```mermaid
graph LR
    A[Start: Payroll Module] --> B[Select Month & Year]
    B --> C[Fetch Attendance Data]
    C --> D[Calculate Base Salary]
    D --> E[Apply Deductions]
    E --> F{Review Sheet}
    
    subgraph Calculation Engine
    E1[Tax]
    E2[Provident Fund]
    E3[Absent Days]
    E4[Loan/Advance]
    end
    
    D --> E1 --> E
    D --> E2 --> E
    D --> E3 --> E
    D --> E4 --> E
    
    F -->|Corrections Needed| G[Manual Adjustment]
    G --> F
    
    F -->|Approved| H[Finalize Salary Sheet]
    H --> I[Generate Bank Templates]
    H --> J[Email Payslips to Employees]
    H --> K[Update Financial Ledger]
```

## 4. Expense Claim Workflow
*How an employee claims reimbursement.*

```mermaid
stateDiagram-v2
    [*] --> Draft
    Draft --> Submitted: Employee Submits w/ Receipt
    Submitted --> SupervisorReview
    
    state SupervisorReview {
        [*] --> Pending
        Pending --> Rejected: Incomplete Info
        Pending --> Approved: Valid Claim
    }
    
    SupervisorReview --> FinanceReview: If Approved
    
    state FinanceReview {
        [*] --> Verification
        Verification --> DisbursementQueue: Verified
        DisbursementQueue --> Paid: Bank Transfer Complete
    }
    
    Paid --> [*]
    Rejected --> [*]
```

## 5. Employee Onboarding Flow (New)
*The critical path of adding a new hire to the system.*

```mermaid
graph TD
    A[Start: Add Employee] --> B{Entry Method}
    B -->|Manual Form| C[Fill Basic Info]
    B -->|Bulk Import| D[Upload CSV]
    
    C --> E[System Generates Employee ID (Auto)]
    E --> F[Select Branch/Dept/Designation]
    F --> G[Set Salary & Bank Details]
    G --> H[Upload Documents (CV/NID)]
    
    H --> I{Create User Account?}
    I -->|Yes| J[Auto-Generate Email & Password]
    I -->|No| K[Profile Active (No Login)]
    
    J --> L[Send Welcome Email with Creds]
    L --> M[Onboarding Complete]
    K --> M
```

## 6. Attendance Correction Request (New)
*Handling "Forgot to punch" scenarios.*

```mermaid
sequenceDiagram
    actor Emp as Employee
    participant Sys as ERP System
    actor Sup as Supervisor

    Emp->>Sys: View Attendance Report
    Emp->>Sys: Select "Absent" Date -> Request Manual Entry
    
    Sys->>Emp: Form (Check-In Time, Check-Out Time, Reason)
    Emp->>Sys: Submit Request
    
    Sys->>Sup: Notify "Correction Request"
    
    Sup->>Sys: Review vs Offline Records
    alt Rejected
        Sup-->>Sys: Reject
        Sys-->>Emp: Notify "Request Denied"
    else Approved
        Sup-->>Sys: Approve
        Sys->>Sys: Update Log Status (Absent -> Present)
        Sys->>Sys: Recalculate Late/Overtime
        Sys-->>Emp: Notify "Attendance Updated"
    end
```

## 7. Other Standard Flows
*Simpler CRUD operations that follow standard patterns:*
*   **Notice Creation:** Draft -> Select Audience -> Publish.
*   **Policy Management:** Draft -> Senior Mgmt Approval -> Publish to Dashboard.
*   **User Role Management:** Add User -> Assign Role -> Save.

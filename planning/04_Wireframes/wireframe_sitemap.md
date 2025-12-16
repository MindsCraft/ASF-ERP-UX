# Wireframe Master Plan & Sitemap
**Status:** In Progress
**Legend:** 🟢 = Completed | 🟡 = To Do

This map visualizes the specific screens (Wireframes) connected to each module.

```mermaid
graph TD
    %% Main Nodes
    Root[**ASF ERP: HRM Module**]:::root
    
    %% Modules
    Root --> Dash[**Dashboard**]
    Root --> Emp[**Employee Mgmt**]
    Root --> Leave[**Leave Mgmt**]
    Root --> Att[**Attendance**]
    Root --> Pay[**Payroll**]
    Root --> Exp[**Expense**]

    %% Wireframe Screens (Leaves)
    Dash --> W1(W01: Admin Dashboard<br/>Command Center):::done
    
    Emp --> W2(W02: Employee Profile<br/>Tabbed View):::done
    Emp --> W3(W03: Add Employee Wizard<br/>Multi-step Form):::todo
    
    Leave --> W4(W04: Apply Leave Modal<br/>Calendar Interaction):::todo
    Leave --> W5(W05: Approval Queue<br/>Slide-over Drawer):::todo
    
    Att --> W6(W06: Daily Log View<br/>Admin Grid):::todo
    Att --> W7(W07: Correction Request<br/>Employee Form):::todo
    
    Pay --> W8(W08: Monthly Salary Sheet<br/>Complex Data Table):::todo
    
    Exp --> W9(W09: Submit Claim<br/>receipt Upload):::todo

    %% Styling
    classDef root fill:#2d3748,color:#fff,stroke:#1a202c,stroke-width:2px;
    classDef done fill:#d4f7dc,stroke:#26a269,color:#1c4532,stroke-width:2px;
    classDef todo fill:#fff3cd,stroke:#ffc107,color:#533f03,stroke-width:2px;
```

## Prioritized Creation List
1.  **Leave Management** (Most interactive)
2.  **Attendance** (High data volume)
3.  **Payroll** (Complex grid)
4.  **Expense** (File handling)

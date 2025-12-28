© 2025 As-Sunnah Foundation. All rights reserved.

### System Requirements Specifications

### (SRS)

## As sunnah Foundation ERP System (Version: New)

##### SRS Version 1. 0 ● 09 December 2025


© 2025 As-Sunnah Foundation. All rights reserved.

Page 2 of 42

Preface

**Style Conventions**

The following style conventions are used in this document:

**Bold**

Names of commands, options, programs, processes, services, and utilities

Names of interface elements (such windows, dialog boxes, buttons, fields, and menus)

Interface elements the user selects, clicks, presses, or types

_Italic_

Publication titles referenced in text

Emphasis (for example a new term)

Variables

Courier

System output, such as an error message or script

URLs, complete paths, filenames, prompts, and syntax

_Courier italic_

Variables on command line

User input variables

< > Angle brackets enclose parameter or variable values supplied by the user

[ ] Square brackets enclose optional values

| Vertical bar indicates alternate selections - the bar means “or”

{ } Braces indicate content that you must specify (that is, x or y or z)


© 2025 As-Sunnah Foundation. All rights reserved.

##### Change history

```
Date Version Created by Description of change
17 - Nov - 2025 1.0 Technical Business Analyst Initial Document
```
```
09 - Dec- 2025 1.1 Technical Business Analyst Updated Document
```
##### Glossary of Terms

```
Term/Acronym Definition
```
```
Constrains Constraint is something that limits or controls the scopes
```
```
Assumption Thing that is accepted as true or as certain to happen,
without proof
```
```
Dependencies Dependency is additional code that a programmer wants
to call
```
```
SRS System Requirement Specification documument
```
```
Dashboard Visual interface showing key HR insights such as headcount,
attendance, leave, payroll, etc.
```
```
Biometric Integration Linking fingerprint/face recognition devices to record
attendance automatically.
```
```
ATS Applicant Tracking System
```
```
Hierarchy Organizational structure showing reporting lines and roles
```
```
KPI Key Performance Indicator
```
```
OT Overtime- Extra working hours eligible for compensation as
per policy
```
```
Performance Appraisal Periodic evaluation process of employees by
managers/HR.
```
```
Payroll Module for salary processing, tax, deductions, payslips, and
disbursement
```

**Introduction**

The introduction of the Software Requirements Specification (SRS) provides an

overview of the entire SRS with purpose, scope, definitions, acronyms, abbreviations,

references, and overview of the SRS. The aim of this document is to gather and analyze

and give an in-depth insight of the complete **ASF ERP system** by defining the problem

statement in detail. Nevertheless, it also concentrates on the capabilities required by

stakeholders and their needs while defining high-level product features. The detailed

requirements of the **ASF ERP system** are provided in this document.

```
1.1 Purpose of this document
```
The purpose of the document is to collect and analyze all assorted ideas that have

come up to define the system, its requirements with respect to end users and

stakeholders. Also, we shall predict and sort out how we hope this product will be used

to gain a better understanding of the project, outline concepts that may be

developed later, and document ideas that are being considered, but may be

discarded as the product develops.

In short, the purpose of this SRS document is to provide a detailed overview of our

software product, its parameters, and goals. This document describes the project's

target audience and its user interface, hardware, and software requirements. It

defines how our client, team and audience see the product and its functionality.

Nonetheless, it helps any designer and developer to assist in software delivery lifecycle

(SDLC) processes.

```
1.2 Scope of HRM Module
```
To automate daily operation of the As-sunnah foundation we will develop a ERP

system which will cover the below modules:

- Human Resource Management System ( **HRM** )
- Training Center Management system ( **TCMS** )
- Accounts Management System ( **AMS** )
- Asset Management System ( **AMS** )
- Charity and Social Service ( **CSS** ) Project Management system
- Purchase and Procurement system ( **PMS** )

Human Resource Management System (HRM) Module:

The ERP-HRM module for ASF Office serves as a **centralized human resource**

**management system** that manages complete employee information and automates

core HR processes across multiple institutions and branches. The module covers:

- Employee Administration
- Attendance Management


- Leave Management
- Payroll Management
- Provident Fund
- Expense Management
- Notice & Notifications
- User & Security Management

Scope includes

In Scope

- Workforce administration (employee master data, hierarchy, roles, branches,
    departments, institutions)
- Time and attendance with biometric login/logout tracking
- Leave automation with approval workflows and leave balance tracking
- Monthly payroll including salary breakdown, statutory deductions, arrear, tax,
    and allowances
- Employee financial contributions (Provident Fund – employer & employee)
- Expense claims and reimbursements with category management and reporting
- Internal engagement & communication (Digital notice board, SMS/email alerts)
- Security and user role governance (role-based authentication, unlimited user
    creation, profile & password management)

Scope excludes

Mobile App

Data analytics like Power BI reporting, ETL Pipeline development

```
1.3 Overview
```
```
The remaining sections of this document provide a general description, including
characteristics of the users of this application, the application's hardware, and the
functional and data requirements of the application. General description of the
project is discussed in section 1.4 of this document. Section 3 gives the functional
requirements, data requirements and constraints and assumptions made while
designing the ASF ERP system. It also gives the user viewpoint of the product. Section
3 also gives the specific requirements of the product. Section 3 also discusses the
external interface requirements and gives detailed description of functional
requirements. Section 4 is for system requirements.
```

```
1.4 Overall Description
```
This document contains the problem statement that the key stakeholders are facing

which is hampering the uninterrupted human resource management process. It further

contains a list of the stakeholders and users of the proposed solution. It also illustrates

the needs and wants of the stakeholders that were identified in the brainstorming

exercise as part of the requirements gathering workshop. It further lists and briefly

describes the major features and a brief description of each of the proposed system

features for the web versions.

The following SRS contains the detail product perspective from different stakeholders.

It provides the detail product functions of ASF ERP system with user characteristics

permitted constraints, assumptions and dependencies and requirements subsets

```
1.5 Assumptions
```
The functional requirements and use cases defined in this document are based upon

the following assumptions:

```
Ref # Assumption Impact
US_ASM_001 Resources:
```
- End users will be
    available to test
    during the time
    they agreed to
- Training
    environment will
    be available in the
    cloud and offline
    as needed

```
Handover, go live and
final signoff
```
```
US_ASM_002 Delivery:
```
- Project environment
    fully configured and
    available as
    expected
- Test cases created,
    training environment
    configured and
    available in the cloud
    and offline

```
Handover, go live and
final signoff
```

US_ASM_003 Budget:

- Project costs will stay the
    same as initially
    budgeted costs
- Training will be
    conducted internally
    with no additional
    training costs incurred

```
Project budget
```
US_ASM_004 Finances:

- Funding for
    development will be
    available when
    needed

```
Implementation
```
US_ASM_005 Scope:

- The project scope will
    not change once the
    stakeholders sign off
    on the scope
    statement

```
Project scope
```
US_ASM_006 Schedule:

- Materials and other third-
    party tools will be
    available as planned
    within the project
    schedule
- Offshore development
    contracts will be fully
    executed within 2 weeks
    of offshore development
    team selection

```
Project completion
```
US_ASM_007 Methodology:

- Project will follow
    Agile Scrum
    methodology
    throughout the
    execution
- Project will follow
    team governance
    guidelines and
    requirements

```
Project execution
```

```
US_ASM_008 Technology:
```
- The team will write the
    solution in MERN Stack
    framework
- The solution will use a new
    test environment setup on
    AWS/GCP
- The solution will be hosted on
    AWS/GCP
- The solution will be installed
    locally
- The solution will work on all
    compatible browsers

```
This will impact the ease
of solution installation
and setup by end-users
```
```
US_ASM_009 Architecture and Design:
```
- The solution will utilize REST
    API architecture
- The solution will reside in an
    offside AWS/GCP cloud

```
1.6 General Constraints
```
```
Constraint Impact
There will be only one system admin in the
system.
```
```
Can create, edit and delete other
Admin users.
The delete operation is available only to the
administrator.
```
```
To reduce the complexity of the
system, there is no check on delete
operation.
System admin will be responsible for data
consistency.
```
```
System admin should be very careful
before deletion of any record
```
```
1.7 Dependencies
```
```
ASF ERP system will operate under the following dependencies:
```
Ref # Dependency Description

US_GLB_DEP_001 MERN full stack developers The successful completion of this
project depends on the
availability of qualified MERN
full-stack developer for the
entire duration of the project


US_GLB_DEP_002 Scopes gathering The successful completion of
the project also depends on the
Business analyst as he need to
gather and verified the scopes
with all stakeholders.

US_GLB_DEP_003 AWS Cloud development
environment

```
Proposed system has
dependency to deploy in the
AWS cloud
```
US_GLB_DEP_004 Third-party REST APIs and
Nodejs modules

```
Proposed system has also
dependency on third-party APIs
and Nodejs Modules
```
US_GLB_DEP_005 SMS, Payment gateway
Integration

```
Developed system need to
integrate with SMS & payment
gateway.
```
US_GLB_DEP_006 Integrations System has dependencies with
other REST APIs integration

US_GLB_DEP_007 Availability of BI report
designer

```
BI reports has data
dependencies and varies user
to users.
```

```
2 Product Functions
```
```
This chapter provides a general description of the product(s) characteristics. It does
not state specific requirements; these sections provide information that makes the
requirements, defined in detail in the following chapters, easier to understand.
```
```
2.1 Product Perspective
```
```
This application will be an online web-based ERP solution with the objective to
automate HRM, Accounts, Training process, assets management, Charity activities
management and other modules as per As-sunnah foundation requirements.
```
```
ASF ERP system should have some core modules that including HRM, Accounts,
Training process, assets management, Charity activities management, user
management & CRM etc.
```
```
SMS, Email and payment gateway integration need to be integrated in this ASF ERP
system for quick notifications and payment process, also need to integrate live chat
as well as in the 2nd phase. The application will be Scalable to integration with any
third-party portal when needed.
```
```
A high-quality web base application needs to develop with dynamic and responsive
user interface, which should be simple and interactive to novice users.
```
```
2.2 Product Functions
```
```
The application produced from these requirements shall functions are as below:
```
Function Description

#1 (^) Admin will add users account to the application database as per
requirements
#2 (^) Super admin feature to add, change, or delete any users account & users
role management.
#3 (^) HR Manager User will be able to register employee in the system, can see
user profile, attendance Management, Leave balance adjustment.
#4 Training Manager can manage the whole Training process and activities
#5 (^) Accounts manager will be able to manage all income, expenses, employee
payroll and other accounting treatment as per accounts module
#6 All charity and social activities will be managed by the manager role from
CSS Module


#7 All purchase, damage and supplier will be managed by procurement
module

# 8 Payment gateway, Instant SMS, Email Notification functionalities will be
implemented

```
2.3 Application Architecture
```

```
2.4 Operating Environment
```
The application operating environment shall be in cloud server as depicted in the

diagram below.

2.4.1 Proposed Application Hosting Environment

2.4.2 Reacts/Nodes Application Steps

```
▪ Initial requirements and package installation
▪ Repository structure
▪ React front-end boiler plate
▪ Nodejs backend boilerplate
▪ Front-end and backend communication
▪ Preparation for deployment to production
▪ Deployment to production
▪ Pushing updates to production application
```

```
2.5 User Characteristics for HRM Module
```
```
Describe the characteristics of user groups who will interact with the system and any
characteristics that might affect the system design are described here:
```
Role Name No. of Users Responsibility / Activity

Super Administrator 1 ▪ Super admin user who creates,
setup and administers portal
general user’s account, admin
and accounting users’ access to
the application.
▪ Create, edit, delete all users
▪ Assign roles & permissions
▪ Create custom user roles
▪ Configure biometric attendance
settings
▪ Manage system parameters
(salary templates, PF rules, tax
settings)
▪ Full access to:

```
o Employees
o Payroll
o Leave
o Attendance
o Expense Management
o Policy
o Notice Board
o Reports
```
HR Administrator 1 ▪ Add new employee

```
▪ Edit employee information
▪ Update employment status
▪ Upload documents (CV, image,
NID, bank info)
▪ View complete employee profile
▪ View attendance logs
▪ Generate attendance reports
▪ Download/export attendance
▪ Leave management
▪ Salary and payroll management
▪ View, verify and manage expense
claims
▪ Can manage notice board
```

###### HR

Manager/supervisor/line
manager

```
Unknown Uses the application as follows
▪ View team employee list
▪ View basic employee profile
▪ Approve/Reject leave for direct
reports
▪ View employees’ attendance
summary
▪ Monitor team expense claims &
approve (if applicable)
▪ View notices relevant to
department
▪ Generate reports related to their
teams
```
HR Officer Unknown ▪ Able to see and update profile

```
▪ View team employee list
▪ View basic employee profile
▪ Can see attendance details
▪ Able to add claim expense
▪ Can view notices
▪ View reports as per role permission
```
Accounts / Finance
Officer

```
Unknown ▪ View payroll list
▪ Process monthly salary
▪ Verify salary calculations
▪ Disburse salary
(bank/cash/cheque)
▪ Upload bank templates
▪ Generate pays lips & send by
email
▪ Manage employer & employee PF
contributions
▪ Review and approve expense
claims
▪ Generate payroll, PF & Tax report
```

Employee Unknown ▪ Submit leave applications

```
View leave balance & leave
history
▪ View attendance
percentage/history
▪ Submit expense claims
▪ Upload expense proof documents
▪ View own profile (limited fields)
▪ Download salary slips
▪ View notices from Admin
Change their account password
```
```
Table ( 1 ) — User Roles
```

3 Detailed Functional Requirements

In this chapter, the functional requirements associated with a feature will be described

for the **ASF ERP system (HRM)**. These are the software capabilities that must be present

for the user to perform the services provided by the feature.

The following sub- sections contain all the software requirements to a level of detail

sufficient to enable designers to design, develop **ASF ERP system (HRM)** and testers to

test the system to satisfy those requirements.

This section specifies-at a minimum-the transformation of inputs into outputs and all

functions performed by the system in response to an input or in support of an output.

This description may consist of a model of the requirements, such as **_data flow_**

**_diagrams_** and **_use cases_** ,

```
3.1 User signup and login
```
###### FRS REQ ID FRS 001

```
REQ Title Users sign up & login system
User Story As a user I want to sign up in the system and want to login as well.
Current Scope Not available
Proposed
Scope
```
```
As per the business requirements system will allow to sign up and log in.
```
**_Functional Requirements Specification:_**

```
Functional
rule (FRS001)
```
- User signup and login
    1) Google SSO
    2) Email Signup page.
- Signup page data field
    1) First Name
    2) Last Name
    3) Email/username (A welcome email will be sent with a
       login bar code after the signup process)
    4) Mobile Phone (OTP verification)
    5) Address
    6) Password
    7) Re-type Password
    8) Role (like role will be “HR manager/Staff”)

```
After the sign-in need a basic setup page before using the
dashboard. Then the user-wise dashboard will be populated.
```

```
Assumptions N/A
Constraints Email verification / OTP
Access
criteria
```
```
Password, email, OPT
```
```
Priority [ Yes ] essential [ ] conditional [ ] optional
```
3.1.1 Use Case of signup & login

Google SSO:


```
3.2 HRM Dashboard Features
```
###### FRS REQ ID FRS

User Story As per the domain and user expectation, we have described some of
HRM dashboard components

REQ Title Dashboard descriptions.

Current Scope Not available

Proposed
Scope

```
As per the business requirements, system will be able to adopt the
below listed core dashboard features as per ASF HRM module
requirements
```

Functional
rule (FRS002)

```
The HRM dashboard will contain some of the features which are
described as follows:
```
```
Employee Statistics
```
- The system must display the total number of current employees.
- The system must display the number of new employees added in
    the current cycle (month).
- The system must show the count of permanent employees.
- The system must show the count of probation employees.
- The system must allow filters (Day, Month, Date Range) for all
    employee statistics.

```
Attendance Summary
```
- The system must display the **total present employees**.
- The system must display the **total absent employees**.
- Filters must be available to generate attendance for **Day, Month,**
    **or Date Range**.

```
Leave Summary
```
- The system must show the total number of leave applications.
- Filters must be available for **Day, Month, or Date Range**.

```
Calendar
```
- The dashboard must include a read-only calendar showing
    holidays, events, and notices.

```
N.B: System will display the user wise specific dashboard based on the
user’s role and permission.
```
Assumptions N/A

Constraints N/A

Access
criteria

```
User role wise access to the respective module
```
Priority [ **Yes** ] essential [ ] conditional [ ] optional


```
3.3 Employee Management Features
```
###### FRS REQ ID FRS

```
User Story HR officer & Manager will be able to use the all the functional facilities
of the employee management features
REQ Title All the functional facilities of the employee management module
Current Scope Not available
Proposed
Scope
```
```
As per change, system will allow to perform all the functional facilities
of the employee management module
```
**_Functional Requirements Specification:_**

```
Functional
rule (FRS003)
```
```
The employee management feature will cover the below features:
```
- The system must allow HR/Admin will be able to enter the
    following fields:

#### Employee Basic Info

- Employee Name
- Employee ID (Auto/Manual generation option)
- Mobile Number
- Email

```
Organizational Details
```
- Select Institution (From predefined list)
    o As-Sunnah Foundation
    o Madrasatus Sunnah
- Select Branch (Branch can be added by admin)
- Select Department
- Select Designation

```
Employment Details
```
- Joining Date
- Employment Status (Probation / Volunteer / Intern / Permanent)
- Salary Information
- Bank Information

```
Personal Information
```
- Date of Birth
- Blood Group
- NID/Passport Number


- Marital Status

Emergency Contact

- Name
- Relationship
- Mobile Number
- Address

Address Details

- Present Address
- Permanent Address

Attachments

- CV upload
- Profile Image upload

Employee List

- System must display a filterable and searchable employee list.
- Users must be able to filter by institution, branch, department,
    designation, status.
- Each row must show basic info (Name, ID, Department, Mobile,
    Status).
- Clicking an employee opens full profile.

Employee Edit

- HR/Admin can edit all fields.
- System must track edit history (optional audit trail).
- Validation must run on all edits.

Employee View Page

System must display all employee information including:

- Profile Picture
- Personal & employment details
- Emergency contact
- Salary info
- Banking info
- Uploaded CV
- Leave Calendar
- Total Days of Employment (auto-calculated)


```
o System must validate required fields before saving.
o System must prevent duplicate Employee IDs (unless manual
override).
o System must store uploaded files securely.
o System will adopt the organizational leave calendar.
o System will display the all-employee related information
based on the roles and permission to other users.
```
```
Assumptions NA
Constraints NA
Access
criteria
```
```
User account & Password
```
```
Priority [ Yes ] essential [ ] conditional [ ] optional
Assumptions NA
Constraints Role access
Access
criteria
```
###### N/A

```
Priority [ Yes ] essential [ ] conditional [ ] optional
```
```
3.4 Payroll Management Module
```
###### FRS REQ ID FRS0 04

```
User Story User will be able to use all the functional facilities of this payroll
management features and process.
REQ Title The functional facilities of this Payroll management
Current Scope Not available
Proposed
Scope
```
```
As per change, the system will allow performing all the functional
facilities of payroll management module and process
```
**_Functional Requirements Specification:_**

```
Functional
rule (FRS011)
```
- Payroll System will be able to calculate the salary structure
    automatically:
       o Gross Salary
       o Basic
       o House Rent
       o Medical
       o Conveyance
       o Provident Fund deductions


- Accounts Manager will be able to enter/configure the
    designation wise salary structure

```
Payroll List View
```
```
Payroll list must include:
```
```
o Serial
o Employee Name
o Designation
o Salary breakup (Basic, House Rent, Medical,
Conveyance)
o Over Time
o Compensation Days
o Gross Salary
o Absent Days
o Tax
o PF Amount
o Net Salary
```
```
Salary Payment
```
- System must allow selecting payment method:
    o Bank
    o Cash
    o Cheque
- Admin must be able to upload bank-specific templates.
- System must generate payment sheets automatically.

```
Salary Pay slip
```
```
Employees, HR and accounts manager must be able to:
```
- View monthly pay slip online.
- Download pay slip as PDF.
- Receive pay slip via email automatically once salary is
    processed.
- See all adjustments, allowances, tax, PF, deductions clearly.

```
Salary Certificate
```
- System must allow HR to create a salary certificate for any
    employee.
- The format must be customizable.
- Must include salary breakdown, tenure, and signature fields.

Assumptions NA


```
Constraints Role access
Access
criteria
```
```
User credentials
```
```
Priority [ Yes ] essential [ ] conditional [ ] optional
```
```
3.5 Leave Management Module
```
###### FRS REQ ID FRS0 05

```
User Story User will be able to use all the functional facilities of leave management
features and process.
REQ Title The functional facilities of this leave application and management
Current Scope Not available
Proposed
Scope
```
```
As per change, the system will allow performing all the functional
facilities of employee leave application and management module
```
**_Functional Requirements Specification:_**

```
Functional
rule (FRS011)
```
```
Leave Dashboard
```
- There will be a leave dashboard in leave management module
    with the below data points:
       o Total Leave Applications
       o Accepted Applications
       o Rejected Applications
       o Pending Applications
- There will be the filtering option by employee, date, supervisor,
    leave type
- Leave application will be available hierarchy wise to the
    respective supervisor dashboard.
- Supervisor will able to accept or reject the leave application

```
Leave Application Submission
```
- In Leave Application from employee basic information fields
    will be auto populated
       o Name
       o ID
       o Department
       o Designation
       o Supervisor details


- Employee will be able to select leave type, leave date, leave
    slot and notes to submit the application
- HR/Accounts/Supervisor will be able to see the short
    information of the employees as below:
       o Personal details
       o Leave data
       o Attendance data
       o Employment status
- HR admin will be able to add leave type/category from the
    system
- Leave Application Approval Workflow

```
o Supervisor must approve/reject leave.
o HR must have override ability.
o System must update leave balance automatically.
o All actions must trigger notification.
```
- System will be able to:
    o Validate leave balance before submission.
    o Notify Supervisor via SMS/Email.
    o Notify HR/Admin for processing.

```
Assumptions NA
Constraints Role access
Access
criteria
```
```
User credentials
```
```
Priority [ Yes ] essential [ ] conditional [ ] optional
```
```
3.6 Attendance Tracking and Management Module
```
###### FRS REQ ID FRS0 06

```
User Story User will be able to use all the functional facilities of attendance
management features.
REQ Title The functional facilities of attendance management and Tracking
Current Scope Not available
Proposed
Scope
```
```
As per change, the system will allow performing all the functional
facilities of employee attendance management module
```
**_Functional Requirements Specification:_**


Functional
rule (FRS011)

- There will be attendance monitoring dashboard under
    attendance tracking module where HR Admin/Manager will be
    able to see the insight of the attendance of the employees.
- The biometrics attendance device need to integrate with the
    attendance Tracking module
- System will be able to track Biometrics/In-Out of the employees
- System must sync data from a biometric attendance device
    daily.
- Each employee’s login/logout timestamps must be stored daily.
- Employee will be able to see only his/her attendance report

```
Attendance View
```
##### HR Admin/Manager will be able to:

- View attendance logs for any employee.
- Filter by date or date range.

```
Attendance Reports
```
```
System will have the facilities to generate the below reports:
```
- Employee wise Attendance summary/tracking reports
- Detailed timestamp logs
- Employee wise Absent reports
- Exporting reports to Excel/PDF

Assumptions NA

Constraints Role access

Access
criteria

```
User credentials
```
Priority [ **Yes** ] essential [ ] conditional [ ] optional

```
3.7 Expense Management
```
###### FRS REQ ID FRS0 07

User Story User will be able to use all the functional facilities of expense
management features.

REQ Title The functional facilities of expense management features

Current Scope Not available


```
Proposed
Scope
```
```
As per change, the system will allow performing all the functional
facilities of employee expense management module
```
**_Functional Requirements Specification:_**

```
Functional
rule (FRS011)
```
- There will be expense monitoring dashboard under expense
    management module where HR Admin/Manager will be able to
    see the insight of the expense of the employees.

```
Expense Claim Submission
```
```
Employees will be able to:
```
```
o Create expense claims
o Select claim category
o Enter amount
o Upload documents (images, PDF, receipts)
```
```
System must:
```
- Route claim to supervisor for approval
- Notify admin after approval

```
Claim Category Management (Admin Only)
```
```
Admin must be able to:
```
- Create new claim categories

```
o Categories Bank Charge
o Advance
o Cash
o Company Tax
o Conveyance
o Purchase
```
- Edit category names
- Set claim limits (optional)

```
Claim Report
```
```
System will be allowed generating reports by:
```
- Date range
- Category
- Status (Pending/Approved/Rejected)


- Report must be exportable (Excel,Word,PDF)

```
Assumptions NA
Constraints Role access
Access
criteria
```
```
User credentials
```
```
Priority [ Yes ] essential [ ] conditional [ ] optional
```
```
3.8 Policy Management Feature
```
###### FRS REQ ID FRS0 08

```
User Story User will be able to use all the functional facilities of policy
management features.
REQ Title The functional facilities of policy management features
Current Scope Not available
Proposed
Scope
```
```
As per change, the system will allow performing all the functional
facilities of employee policy management Features
```
**_Functional Requirements Specification:_**

```
Functional
rule (FRS011)
```
- There will a system feature to configure the policy of the
    organization and the policy must have to approved by senior
    management through the system

```
Calendar Management
```
```
Admin/HR Admin must be able to:
```
- Create office holiday calendar
- Add/edit/delete holiday dates
- Sync holidays to employee dashboards & attendance

```
Salary Structure Rules
```
```
HR/Accounts Admin must be able to:
```
```
o Define salary calculation rules
o Configure percentages for Basic, House Rent, Medical, etc.
o Set PF contribution policies
```

```
o Apply rules across employees or specific groups
```
```
Assumptions NA
Constraints Role access
Access
criteria
```
```
User credentials
```
```
Priority [ Yes ] essential [ ] conditional [ ] optional
```
```
3.9 Notice Board Feature
```
###### FRS REQ ID FRS0 09

```
User Story User will be able to use all the functional facilities of notice board
features.
REQ Title The functional facilities of notice board
Current Scope Not available
Proposed
Scope
```
```
As per change, the system will allow performing all the functional
facilities of Notice board Features
```
**_Functional Requirements Specification:_**

```
Functional
rule (FRS011)
```
- There will a system feature to create the notice of the
    organization and the policy must have to approved by senior
    management through the system

```
Create Notice (HR Admin /Manager Only)
```
```
Admin will be able to do the below action in the notice board
feature:
```
- Create a notice
- Attach documents
- Set visibility to:
    o Individual employee
    o Department
    o Branch
    o All employees
- System will have the facility to export of notices by date range


```
View Notices
```
```
All employees must see:
```
```
o Title
o Description
o Attachments
```
##### o Published date

```
Assumptions NA
Constraints Role access
Access
criteria
```
```
User credentials
```
```
Priority [ Yes ] essential [ ] conditional [ ] optional
```
```
3.10 User Management Module
```
###### FRS REQ ID FRS 010

```
User Story User will be able to manage all the system users using this feature
REQ Title The functional facilities of user management
Current Scope Not available
Proposed
Scope
```
```
As per change, the system will allow performing all the functional
facilities of user management
```
**_Functional Requirements Specification:_**

```
Functional
rule (FRS011)
```
- HR admin/System admin will be able to use the all user
    management features
- All user information will be editable by the HR Admin or system
    admin

##### User Account Management

```
The system must allow HR Admin to:
```
1. Create new user accounts.
2. Enter user details:


```
o Name
o Email
o Mobile
o Employee ID (linked to Employee Module)
o Role Assignment
o Status (Active/Inactive)
```
3. Edit user details (except password).
4. Activate/Deactivate user accounts.
5. Delete users (soft delete recommended).
6. Search and filter users by:
    o Name
    o Employee ID
    o Role
    o Status

System behavior:

- User cannot log in until account is activated.
- Deleted user cannot access the system.
- Inactive user receives error "Account Disabled."

Role Management

System must provide predefined roles, e.g.:

- Admin
- HR Admin
- Supervisor
- Employee
- Finance/Payroll
- Custom Roles (Created by Admin)

Capabilities including:

- Add/Edit/Delete Employee
- Approve Leave
- View Payroll
- Edit Salary Structure
- Access Dashboard
- Manage Notices
- View Attendance
- Approve Claims
- Edit Policies

Role-wise Authentication & Permission Control

The system must enforce:

```
o Page-level access control
```

```
o Module-level access control
o Action-level permission (Create/Read/Update/Delete)
o Feature-level access control (Example: Salary breakdown view
only allowed for Payroll role)
```
##### User Profile Management

```
The system must allow users to:
```
```
o View:
```
1. Image
2. Name
3. Employee ID
4. Email
5. Mobile
6. Attendance Percentage
7. Leave Claimed/Remaining
8. Employment Status
o Update:
1. Password ONLY (by HR admin)

Assumptions NA

Constraints Role access

Access
criteria

```
User credentials
```
Priority [ **Yes** ] essential [ ] conditional [ ] optional

```
3.11 Report Module
```
###### FRS REQ ID FRS 011

User Story Admin/HR/Accounts User will be able to export the customize reports

REQ Title The functional features of reporting Module

Current Scope Not available

Proposed
Scope

```
As per change, the system will allow performing all the functional
facilities to prepare and visualize reports based on user type
```

**_Functional Requirements Specification:_**

```
Functional
rule (FRS011)
```
```
The Report Module must:
```
- Provide consolidated reporting for all major modules.
- Allow users to apply dynamic filters (department, branch,
    employee, date range, etc.).
- Provide multiple export formats:
    o **PDF**
    o **Excel (XLSX)**
    o **CSV**
- Allow users with proper permissions to schedule reports
    (Optional).
- Offer secure access based on user role and permissions.
- Maintain consistency across all HRM modules

```
Report Categories
```
```
The Report Module must include reports from the following modules:
```
- Employee Reports

```
o Employee Basic Information Report
o Employee Status Report
(Probation/Permanent/Intern/Volunteer)
o New Employee Report
o Employee Separation (Inactive) Report
o Department-wise Employee Distribution
o Branch-wise Employee Distribution
```
- Attendance Reports

```
o Daily Attendance Summary
o Date Range Attendance Report
o Employee-wise Attendance History
o Late Entry Report
o Early Exit Report
o Absent Report
o Monthly Attendance Summary
o Biometrics-Based Raw Log Report
```
- Leave Reports

```
o Leave Application Summary
(Accepted/Rejected/Pending)
o Employee-wise Leave Balance Report
o Leave Type Usage Report (Casual, Annual, Medical,
Maternity, etc.)
o Department-wise Leave Report
```

```
o Supervisor Approval Time/Response Report
```
- Payroll Reports

```
o Monthly Payroll Sheet
o Salary Breakdown Report
o Tax Deduction Report
o Provident Fund Contribution Report
o Over Time Report
o Compensation Workday Report
o Bank Payment Sheet (Based on Template)
o Salary Disbursement Status Report (Paid/Unpaid)
```
- Expense Reports

```
o Expense Claim Report
o Category-wise Expense Report
o Approved/Rejected/Pending Claim Report
o Employee-wise Expense Summary
o Date Range Expense Analytics
```
- Notice Board Reports

```
o Department/Branch Notice Report
```
- User Management Reports

```
o System User List
o Active/Inactive User Report
o User Login History Report
o Failed Login Attempt Report
```
##### o Password Reset Log Report

Assumptions NA

Constraints Role access to module

Access
criteria

```
User credentials
```
Priority [ **Yes** ] essential [ ] conditional [ ] optional



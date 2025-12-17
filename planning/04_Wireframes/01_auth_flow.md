# Wireframe W01: User Signup & Login
**Requirement ID:** FRS001
**Role:** Unauthenticated User

![Auth Sequence](../assets/wireframe_auth_master.png)

## 1. Visual Layout
**Structure:** Split-Screen Layout.
*   **Left (35%):** Brand Identity (Logo, Welcome Message).
*   **Right (65%):** Authentication Card (Center Aligned).

## 2. Detailed Technical Specification
This wireframe strictly implements the data fields defined in **FRS001**.

### 2.1 State: Sign In (Default)
**Goal:** Authenticate existing users.

| Field Label | Input Type | Validation Rule |
| :--- | :--- | :--- |
| **Email Address** | Text (Email) | Valid email format. |
| **Password** | Password | Min 8 chars. |
| **Remember Me** | Checkbox | Optional. |

**Actions:**
*   [Primary] **Sign In**: Validates and redirects to Dashboard (FRS002).
*   [Secondary] **Continue with Google**: Triggers SSO flow.
*   [Link] **Forgot Password?**: Initiates recovery.
*   [Toggle] **Don't have an account? Sign Up**: Switches to State 2.2.

### 2.2 State: Sign Up (Registration)
**Goal:** onboard new users for Admin Approval.

| Ref | Field Label | Input Type | Mandatory? | Notes |
| :--- | :--- | :--- | :--- | :--- |
| **1** | **First Name** | Text | Yes | |
| **2** | **Last Name** | Text | Yes | |
| **3** | **Mobile Number** | Tel | Yes | Triggers OTP (Simulated). |
| **4** | **Email / Username** | Text | Yes | Unique ID check. |
| **5** | **Address** | Text Area | Yes | As per FRS001.5. |
| **6** | **Password** | Password | Yes | |
| **7** | **Confirm Password** | Password | Yes | Must match Field 6. |
| **8** | **Role Request** | Dropdown | Yes | e.g. "HR Manager", "Staff". |

**Actions:**
*   [Primary] **Create Account**:
    1.  Validates all fields.
    2.  Sets status to `Pending Approval`.
    3.  Shows Toast: *"Registration Submitted. Waiting for Admin Approval."*

## 3. SRS Alignment Check
*   ✅ **Methods:** Google SSO & Email included.
*   ✅ **Fields:** First Name, Last Name, Mobile, Address, Role included explicitly.
*   ✅ **Flow:** Login -> Dashboard connection established.

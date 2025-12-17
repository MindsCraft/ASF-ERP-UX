# Wireframe W09: Notice Board
**Requirement ID:** FRS009
**Role:** All Users (Reader) / HR Admin (Publisher)

*(Visual Placeholder: Image Generation Quota Paused)*

## 1. Screen 9.0: Notice Feed (Public View)
**Goal:** Internal communication hub.

**Layout:** Card Stream.
*   **Card:** [Pinned Icon] **"Office Closed for Eid"**
    *   *Published:* 2 Hours ago.
    *   *Body:* Preview text (2 lines).
    *   *Action:* [Read More] -> Expands modal.

## 2. Screen 9.1: Create Notice (Admin View)
**Goal:** Publish announcements.

**Form:**
*   **Title:** [Text Input]
*   **Description:** [Rich Text Editor]
*   **Target Audience:**
    *   (Radios: All Employees / Specific Branch / Specific Dept).
    *   If Specific -> Show [Dropdown].
*   **Attachments:** [File Upload] (PDF/Image).
*   **Action:** [Publish Notice].

## 3. SRS Alignment Check
*   ✅ **Targeting:** Branch/Dept selector matches FRS009.3.
*   ✅ **Access:** Visibility logic (FRS009.4) defined in specs.

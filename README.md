# Planner Onboarding Task Reminder

## What This Project Is
This repository documents a Microsoft Power Automate cloud flow that sends scheduled email reminders for onboarding tasks that are still incomplete in Microsoft Planner.

The flow helps ensure onboarding tasks are not forgotten by automatically notifying users when action is still required.

---

## Why This Exists
Onboarding tasks are often created in Microsoft Planner but can be missed when users do not regularly check their task list.

This automation removes the need for manual follow-ups by automatically surfacing pending tasks through email reminders.

---

## How the Flow Works
The automation runs on a schedule and performs the following steps:

1. Retrieves all Planner tasks assigned to the signed-in user  
2. Filters out tasks that are already completed (`percentComplete = 100`)  
3. Loops through the remaining incomplete tasks  
4. Sends an email reminder for each incomplete task  

Planner remains the source of truth for task status, while Power Automate handles the reminder logic.

---

## Flow Structure

Recurrence
↓

List my tasks (Planner)
↓

Filter array (incomplete tasks only)
↓

Apply to each
↓

Send email reminder


---

## Platform Context
- **Power Automate** is used for scheduling and automation logic  
- **Microsoft Planner** is used for task management  
- **Outlook** is used to send email notifications  

Planner is a Microsoft 365 service and integrates with Power Automate via a standard connector.

---

## Limitations
- Microsoft Teams notifications were not included due to tenant restrictions  
- The flow processes tasks assigned to the signed-in user only  

---

## Repository Contents

/screenshots → Visual references of the flow configuration
README.md → Project documentation


---

## Status
✔️ Flow built  
✔️ Tested successfully  
✔️ Documented

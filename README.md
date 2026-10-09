# AI Law Firm Automation

An AI-powered law firm automation built with n8n, Google Gemini, ClickUp, Google Drive, Gmail, and Telegram.

## Overview

This automation streamlines client intake, case organization, notice drafting, lawyer approval, and hearing reminders.

When a client submits the intake form, the workflow processes the information using AI, creates a case record in ClickUp, creates a Google Drive folder, and sends email notifications to the lawyer and client.

It also prepares a notice draft for lawyer review. The notice is emailed to the client only after approval through Telegram.

A separate scheduled workflow checks upcoming hearing dates and sends reminders through Telegram and Gmail.

## Workflow

### 1. Client Intake and Notice Approval

Client Intake Form → AI Case Triage → Assign Case Details → Create ClickUp Case → Create Google Drive Case Folder → Email Lawyer → Email Client Confirmation → AI Notice Drafter → Create ClickUp Notice Draft → Request Lawyer Approval on Telegram → Check Approval

- **Approved:** Email the approved notice to the client.
- **Not approved:** Email the lawyer that revisions are needed.

### 2. Hearing Reminders

Daily 8 AM Schedule → Get ClickUp Hearings for the Next 7 Days → Send Telegram Reminder → Send Email Reminder

The reminder schedule uses the timezone configured in n8n.

## How It Works

1. 📩 **Collect client information**  
   Receive the client's name, contact details, case type, issue description, opposing party, important date, and preferred contact method through an intake form.

2. 🤖 **Process the case with AI**  
   Google Gemini processes the submitted information and produces structured case details, including a summary, urgency, and suggested next step.

3. 📋 **Create a case record**  
   Save the organized case information in ClickUp for tracking and review.

4. 📁 **Create a case folder**  
   Create a dedicated Google Drive folder for organizing case-related files.

5. 📧 **Send initial notifications**  
   Notify the lawyer about the new case and send a confirmation email to the client.

6. 📝 **Generate a notice draft**  
   Prepare an AI-generated notice draft and save it in ClickUp for lawyer review.

7. ✅ **Request lawyer approval**  
   Send the draft for approval through Telegram and wait for the lawyer's response.

8. 🔀 **Handle the approval decision**  
   Email the notice to the client after approval. If it is not approved, notify the lawyer that revisions are needed.

9. ⏰ **Check upcoming hearings**  
   Run a daily check for hearing dates recorded in ClickUp within the next seven days.

10. 🔔 **Send hearing reminders**  
    Deliver reminders through Telegram and Gmail.

## Features

- 📩 Client intake form
- 🤖 AI-powered case summaries and structured information
- 📋 Automatic ClickUp case creation
- 📁 Dedicated Google Drive case folders
- 📧 Lawyer notifications and client confirmation emails
- 📝 AI-generated notice drafts
- ✅ Lawyer approval through Telegram
- 🔀 Approval-based email routing
- ⏰ Scheduled checks for upcoming hearings
- 🔔 Telegram and email reminders

## Technologies Used

- **n8n** — Workflow automation and scheduling
- **Google Gemini** — AI case processing and notice drafting
- **Structured Output Parser** — Structured AI output
- **ClickUp** — Case records, notice drafts, and hearing dates
- **Google Drive** — Case folder organization
- **Gmail** — Notifications, confirmations, and approved notices
- **Telegram** — Lawyer approval and hearing reminders

## Use Case

This automation helps law firms reduce repetitive administrative work by connecting client intake, case records, document drafting, approval handling, and reminders in one workflow.

It can be customized for different intake fields, case types, notice templates, notification recipients, and reminder schedules.

## Important Notes

- This project automates administrative tasks and does not provide legal advice.
- AI-generated summaries and notice drafts require lawyer review.
- The approval step controls whether a notice is emailed to the client.
- Hearing reminders depend on the dates recorded in ClickUp; the workflow does not retrieve dates from court systems.
- Scheduled reminders require an active n8n instance and valid connected credentials.
- Demo data is used for demonstration purposes.

## Demo Video

[Watch the Law Firm Automation Demo](./Law_Firm_Demo_Synced_Voice_Only.mp4)

## Project Status

Completed portfolio demo demonstrating client intake, case management, notice approval, and hearing reminders.

# Gym Management Automation System
**Tools:** n8n | Airtable | Gmail | Telegram | Paystack
**Type:** Business Process Automation
**Industry:** Fitness & Membership Management

## Project Overview
Built 4 automated workflows handling the complete 
gym member lifecycle from registration to subscription 
renewal — eliminating all manual administrative work 
and integrating Paystack for payment processing.

## Workflows Built

### Workflow 1 — Gym Registration

Webhook → HTTP Request (Paystack) → HTTP Request
→ Create Airtable Record → Edit Fields
→ Wait → Send Gmail

- Triggered when new member registers
- Processes payment via Paystack API
- Creates member record in Airtable
- Sends welcome email via Gmail automatically

### Workflow 2 — 3 Days to Expiration Reminder

Schedule Trigger → Search Airtable Records
→ If Condition → Edit Fields
→ Send Gmail + Send Telegram Message
- Runs on schedule automatically
- Searches for members expiring in 3 days
- Sends reminder via both Gmail and Telegram
- Conditional logic handles different scenarios

### Workflow 3 — Expired Subscription
Schedule Trigger → Search Airtable Records
→ If Condition → Update Record
→ Send Gmail
- Automatically detects expired memberships
- Updates member status in Airtable
- Sends expiry notification via Gmail
- Handles active vs expired conditions

### Workflow 4 — Subscription Renewal
Webhook → Search Airtable Records
→ Update Record → Wait → Send Gmail
- Triggered by Paystack renewal payment webhook
- Finds and updates member record automatically
- Sends renewal confirmation email
- Paystack webhook confirms successful payment

## Business Impact
- Zero manual registration processing
- Paystack integration automates payment collection
- Automated expiry reminders reduce membership churn
- Real time subscription status updates
- Multi channel notifications — Email and Telegram
- Complete member lifecycle managed automatically

## Skills Demonstrated
- n8n workflow design
- Paystack payment integration
- Webhook integration
- Airtable database operations
- Conditional logic and branching
- Scheduled automation
- Gmail API integration
- Telegram bot integration
- Multi channel notification system

## Workflow Preview
![Gym Management Automation](gym_automation.jpg)

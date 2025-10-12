# n8n Workflows
This repository contains a collection of n8n workflows designed to automate and optimize key business processes. All workflows leverage AI agents for intelligent task handling and are integrated with Google Sheets and Gmail for seamless data management and communication.

## Workflows Overview

### 1. AI Mentorship Assistant
Folder: AI Mentorship Assistant
Description: Automates mentorship follow-ups by sending personalized, motivational emails to mentees based on their progress in the program.
Features:
- Reads mentee data from Google Sheets.
- Uses AI agent (Google Gemini) to generate personalized follow-up messages.
- Sends emails via Gmail.
- Updates Google Sheets with last follow-up timestamp and status.
- Conditional logic to target only active mentees who require follow-up.

### 2. AI Customer Onboarding Bot
Folder: AI Customer Onboarding Bot
Description: Automates customer onboarding follow-ups with personalized emails according to the current stage in the onboarding process.
Features:
- Fetches customer data from Google Sheets.
- Generates AI-based personalized messages for each customer.
- Sends professional follow-up emails via Gmail.
- Updates onboarding progress and last contact in Google Sheets.
- Conditional logic ensures only relevant customers are contacted.

### 3. Marketing Lead Follow-up Automation
Folder: Marketing-lead-followup-Automation
Description: Streamlines lead management by scoring leads, calculating ROI, and sending AI-generated follow-up emails.
Features:
- Reads marketing leads from Google Sheets CRM.
- Scores leads based on source, campaign, and engagement.
- Uses AI agent to generate short persuasive emails.
- Sends emails through Gmail.
- Updates Google Sheets with status, priority, and last contact.
- Filters leads based on priority to optimize outreach.

### 4. HR Operations AI Assistant
Folder: HR-Operations AI Assistant
Description: Automates HR reporting, including attendance, payroll, and meeting summaries for internal review.
Features:
- Reads employee data from Google Sheets.
- Uses AI agent to summarize attendance, payroll status, and meetings.
- Sends daily HR update emails via Gmail.
- Updates Google Sheets with processed status and timestamps.
- Prioritizes employees requiring attention based on attendance and payroll status.

---

## Key Features Across All Workflows
- AI Integration: Intelligent content generation using Google Gemini through n8n’s AI nodes.
- Automation: Fully automated scheduling via Schedule Trigger node.
- Data Management: Google Sheets integration for storing and updating workflow data.

## Project Structure

n8n-workflows/
│
├─ AI Mentorship Assistant/
│ └─ workflow.json
├─ AI Customer Onboarding Bot/
│ └─ workflow.json
├─ Marketing-lead-followup-Automation/
│ └─ workflow.json
├─ HR-Operations AI Assistant/
│ └─ workflow.json
└─ README.md

## Notes for Setup
1. **Credentials:**  
   - Each workflow requires **Google Sheets** and **Gmail** credentials.  
   - AI agent nodes require proper API access (Google Gemini or OpenAI) configured in n8n.
2. **Importing Workflows:**  
   - Use `Import` option in n8n to add JSON workflow files.  
   - Ensure credentials are linked after import before running workflows.
3. **Scheduling:**  
   - All workflows use `Schedule Trigger` nodes. Adjust cron expressions as per your timezone and requirements.
4. **Testing:**  
   - Test each workflow with a sample sheet before running on live data to avoid accidental emails or data updates.


This setup allows you to run **AI-powered automated workflows** for Mentorship, Customer Onboarding, Marketing, and HR operations efficiently and professionally.

- Communication: Gmail integration for sending personalized emails automatically.
- Conditional Logic: Ensures actions are performed only when specific criteria are met.

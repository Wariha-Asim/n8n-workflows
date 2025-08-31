## Job Application Automation Tracker

This repository contains an n8n automation workflow that streamlines job application management by integrating Google Sheets, Gmail, Discord, and Notion. Multiple automations are included to manage applications efficiently.

## Features

Google Sheets Trigger: Automatically detects new job applications submitted via Google Forms.

Email Notifications: Sends acknowledgment emails to candidates and notifies HR of new applications.

Position-Based Workflow: Routes applications according to the position applied for using a switch node.

Discord Notifications: Sends detailed candidate application info to a Discord channel.

Notion Database Integration: Logs every application into a Notion database with candidate details including Name, Email, Position, Resume, and WhatsApp Number.

## Prerequisites

n8n instance (self-hosted or cloud)

Google Sheets with job application form responses

Gmail account for sending emails

Discord webhook for notifications

Notion account and a database for storing applications

Node.js (if self-hosting n8n)

Setup Guide

## Clone the Repository:

git clone https://github.com/Wariha-Asim/n8n-workflows/tree/main/Job%20Application%20Automation%20Tracker

## Import Workflow into n8n:

Open your n8n instance

Click Import → JSON

Select workflow.json from this project

## Configure Credentials:

Set up Google Sheets, Gmail, Discord, and Notion credentials in n8n

Replace placeholders like GOOGLE_SHEETS_DOCUMENT_ID and NOTION_DATABASE_ID with your actual IDs

## Activate Workflow:

Test the workflow by submitting a dummy application in your Google Form

Ensure emails, Discord notifications, and Notion entries are created correctly

## Safety & Privacy

No personal data or credentials are included in this workflow.

All sensitive information (IDs, emails, tokens) are placeholders.

Safe to push and share on GitHub.

## Repository Structure
n8n-workflows/
│
├─ Job Application Automation Tracker/
│   ├─ workflow.json           # n8n workflow JSON file
│   └─ README.md               # Documentation

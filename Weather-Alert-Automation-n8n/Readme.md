# 🌦️ Weather Alert Automation Workflow (n8n)

This repository contains an **n8n workflow** that fetches weather data for multiple cities using the OpenWeatherMap API, evaluates conditions (e.g., high temperature or cloudy weather), sends alerts to Discord, and logs results into Google Sheets.


## 🚀 Features
- Fetches real-time weather data for multiple cities.
- Evaluates alerts based on:
  - 🌡 Temperature > 30°C
  - ☁️ Overcast cloud conditions
- Sends notifications to **Discord** via webhook.
- Stores weather data into **Google Sheets** for historical tracking.
- Runs automatically on a **daily schedule at 12:00 PM**.


## 📋 Prerequisites
Before importing the workflow, make sure you have:
1. [n8n](https://n8n.io/) installed and running (self-hosted or cloud).
2. An **OpenWeatherMap API key** ([get it here](https://openweathermap.org/api)).
3. A **Discord Webhook URL** (to post alerts).
4. Access to a **Google Sheet** (and connected Google account via n8n credentials).


## ⚙️ Setup Instructions
1. Clone this repository:
   git clone git clone https://github.com/Wariha-Asim/n8n-workflows.git
cd n8n-workflows/Weather-Alert-Automation-n8n

Open n8n → Import the weather-alert-workflow.json file.

Configure credentials in n8n:

Replace {{OPENWEATHER_API_KEY}} with your OpenWeatherMap API key.

Replace {{DISCORD_WEBHOOK_ID}} with your Discord Webhook credentials.

Replace {{GOOGLE_SHEET_ID}} with your Google Sheet ID.

Replace {{GOOGLE_SHEETS_AUTH_ID}} with your Google Sheets OAuth credentials.

Save and activate the workflow.

The workflow will now run automatically every day at 12:00 PM.

## 🗂 Data Flow

Schedule Trigger → Runs workflow daily.

Cities Function → Generates a list of cities.

HTTP Request → Calls OpenWeatherMap API.

Set Node → Extracts date, city, temperature, and condition.

IF Node → Checks conditions (Temp > 30 OR Overcast clouds).

Discord Node → Sends alert if condition met.

Google Sheets Node → Logs results.

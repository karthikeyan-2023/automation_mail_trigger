

##📩 Automated Email Notification Workflow using n8n

This repository contains an n8n workflow that automates sending confirmation emails using Gmail based on data fetched from Google Sheets. The workflow is designed to streamline communication for events, workshops, or registrations without manual intervention. 

Mail Trigger

🚀 Features

✔️ Fetches rows dynamically from a Google Sheet
✔️ Iterates over each row to extract user data
✔️ Sends personalized email confirmations via Gmail
✔️ Includes a configurable waiting interval between messages
✔️ Can be executed manually or scheduled at a specific time
✔️ Prevents spam by batching emails instead of sending all at once

🧱 Workflow Architecture

The workflow is composed of the following nodes:

Node	Purpose
Manual Trigger	Start workflow on-demand from n8n UI
Schedule Trigger	Runs the workflow automatically at a defined time every day
Google Sheets – Get Rows	Reads attendee details from Sheet1
Split in Batches	Loops through each record without overloading Gmail
Wait Node	Adds a delay of 2 minutes before sending the next email
Gmail – Send Message	Sends confirmation email to each participant
🖥️ How It Works

The workflow starts manually or at the scheduled hour (10 AM daily)

It retrieves rows from the Google Sheet containing user emails

It processes each entry one-by-one using Split in Batches

For every record:

The system waits for 2 minutes

Sends an event confirmation email via Gmail

Repeats until all emails are sent

📧 Email Template Used

Subject:

Your Seat is Confirmed – AI-Powered Digital Marketing Workshop


Message body can be customized directly inside Gmail node settings.

⚙️ Requirements
Dependency	Purpose
n8n	Workflow automation engine
Google Sheets OAuth Credentials	To access sheet data
Gmail OAuth Credentials	To send automated emails
🛠️ Setup Instructions

Clone this repo

Import the JSON workflow into your n8n instance

Add Google Sheets and Gmail OAuth credentials

Update Sheet ID or Gmail message if needed

Activate the workflow

🗂️ Use Cases

🔥 Event registration confirmations
📅 Webinar/Workshop seat approvals
🎟 Subscription or onboarding emails
📢 Batch notifications without manual effort

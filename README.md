# 📩 Automated Email Notification Workflow (n8n)

This repository contains an n8n workflow that automatically sends confirmation emails using Gmail based on user data stored in Google Sheets. The workflow reduces manual effort and ensures every participant receives timely email communication. 

---

## 📘 Project Overview

This workflow was built using **n8n**, an open-source automation tool. It reads participant details from a Google Sheet and sends an email confirmation to each user using Gmail.

---

## 🚀 Features

- Automatically fetches user data from Google Sheets
- Sends confirmation emails via Gmail
- Processes participants in batches
- Adds a delay between emails to avoid spam
- Can run manually or at a scheduled time (10 AM daily)

---

## 🧱 Workflow Components

| Node                       | Function                                             |
|---------------------------|-------------------------------------------------------|
| Manual Trigger             | Start workflow manually                               |
| Schedule Trigger           | Run workflow daily at 10 AM                           |
| Google Sheets: Get Rows    | Retrieve participant details from sheet               |
| Split In Batches           | Loop through each participant record                  |
| Wait                       | Delay execution for 2 minutes                         |
| Gmail Send Message         | Send confirmation email to each participant           |

---

## ⚙️ How It Works

1. Workflow is triggered manually or by schedule
2. Reads all rows from a Google Sheet
3. Loops through each row in batches
4. Waits 2 minutes between every email
5. Sends Gmail confirmation to each user
6. Repeats until all records are processed

---

## ✉️ Email Format

**Subject**


**Body**
Configured inside Gmail node (customizable)

---

## 🛠 Requirements

- n8n instance (Cloud or Self-hosted)
- Google Sheets OAuth credentials
- Gmail OAuth credentials

---

## 📦 Setup Instructions

1. Import the JSON workflow into n8n
2. Connect Google Sheets and Gmail credentials
3. Update the Google Sheet ID if required
4. Activate the workflow
5. Run manually or let it execute on schedule

---

## 🎯 Use Cases

- Workshop / Event registration confirmations
- Automated follow-up emails
- Student onboarding sequences
- Bulk announcements without manual effort

---

## 🏁 Conclusion

This n8n workflow transforms email confirmation into an automated process, saving time and ensuring consistent communication. It is scalable, customizable, and easy to modify for any event-based automation task.

---

### ⭐ Support

If you like this project, please **star the repository** ⭐ and share it!


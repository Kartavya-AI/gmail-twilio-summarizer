# 📩 Gmail → Twilio WhatsApp Summarizer

An **n8n workflow** that automatically:
- Fetches Gmail messages  
- Summarizes them using **Google Gemini AI**  
- Sends a structured daily digest to **WhatsApp via Twilio**  

Stay on top of your inbox with clear, AI-powered WhatsApp summaries every day.

---

## ✨ Features
- Fetches Gmail emails on a schedule (daily, hourly, or custom)  
- Uses **Google Gemini AI** to generate short, human-friendly summaries  
- Sends WhatsApp messages through **Twilio API**  
- Easy to import & customize in **n8n**  
- Outputs clean and structured summaries  

---

## 📂 Repository Structure
gmail-twilio-summarizer/
├── workflow.json # Exported n8n workflow
├── README.md # Documentation

markdown
Copy code

---

## 🚀 Setup Instructions

### 1. Import Workflow
- Open your n8n instance  
- Go to **Workflows → Import from File**  
- Upload `workflow.json`  

### 2. Configure Credentials
Inside n8n, set up these credentials:
- **Gmail (OAuth2)** → Fetch emails  
- **Google Gemini API** → Summarize content  
- **Twilio** → Send WhatsApp messages  

### 3. Environment Variables
Add the following values in n8n:
- `GMAIL_OAUTH2`  
- `GOOGLE_GEMINI_API_KEY`  
- `TWILIO_ACCOUNT_SID`  
- `TWILIO_AUTH_TOKEN`  
- `TWILIO_WHATSAPP_FROM` → e.g. `whatsapp:+14155238886`  
- `TWILIO_WHATSAPP_TO` → e.g. `whatsapp:+91XXXXXXXXXX`  

### 4. Adjust the Schedule
The workflow runs at **8 PM daily** by default.  
Change the **Schedule Trigger** node to fit your needs.  

---

## 📲 Example WhatsApp Output
📩 Daily Email Summary

From: John Doe
Subject: Meeting Tomorrow
Summary: Reminder about the project meeting scheduled at 10 AM.

From: HR Department
Subject: Policy Update
Summary: New leave policy effective from next month.

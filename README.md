# AI FAQ Chatbot with Knowledge Base using n8n

An AI-powered FAQ chatbot built with **n8n** and **Google Gemini AI**. This automation receives questions from Telegram users, retrieves relevant information from a Google Sheets knowledge base, generates accurate responses using AI, logs every conversation to Google Sheets, and replies instantly through Telegram.

---

## 📌 Features

- 💬 Receives questions from Telegram
- 📚 Uses Google Sheets as a dynamic knowledge base
- 🤖 Uses Google Gemini AI to answer FAQs
- 📝 Retrieves and formats FAQ data automatically
- 📊 Logs all conversations into Google Sheets
- 📲 Sends AI-generated replies back to Telegram
- ⚡ Built with Google Gemini AI Agent

---

## 🛠 Workflow

```text
Telegram Trigger
        │
        ▼
Google Sheets (Get FAQ Rows)
        │
        ▼
Code (Format Knowledge Base)
        │
        ▼
Google Gemini AI Agent
        │
        ▼
Telegram
        │
        ▼
Google Sheets (Chat Logs)
```

---

## 🚀 Technologies Used

- n8n
- Telegram Bot API
- Google Gemini API
- Google Sheets API
- JavaScript

---

## 📦 Nodes Used

- Telegram Trigger
- Google Sheets (Get Row(s))
- Code
- AI Agent
- Telegram
- Google Sheets (Append Row)

---

## 🧠 Knowledge Base Structure

The workflow retrieves the following information from Google Sheets:

- Question
- Answer
- Category
- Keywords

---

## 📱 Sample Telegram Conversation

**User**

```
Do you build n8n workflows?
```

**Bot**

```
Yes, we build custom n8n workflows for businesses.
```

---

**User**

```
What are your business hours?
```

**Bot**

```
We are open Monday to Friday, 8:00 AM to 5:00 PM.
```

---

## 📊 Sample Google Sheets (FAQ)

| Question | Answer | Category | Keywords |
|----------|--------|----------|----------|
| What are your business hours? | Monday–Friday, 8:00 AM–5:00 PM | General | hours,time,open |
| Where are you located? | Cebu City, Philippines | General | location,address |
| Do you build n8n workflows? | Yes, we build custom n8n workflows for businesses. | Services | n8n,workflow |
| Do you accept online payments? | GCash, Maya, and bank transfer. | Payments | payment,gcash,maya |

---

## 📊 Sample Chat Logs Sheet

| Timestamp | User | Question | AI Answer |
|-----------|------|----------|-----------|
| 2026-07-08 | Belio | Do you build n8n workflows? | Yes, we build custom n8n workflows for businesses. |
| 2026-07-08 | John | What are your business hours? | Monday–Friday, 8:00 AM–5:00 PM. |

---

## ⚙ Prerequisites

Before importing the workflow, configure the following credentials in n8n:

- Telegram Bot
- Google Gemini API
- Google Sheets

---

## 📂 Google Sheets Setup

Create a spreadsheet with two sheets.

### Sheet 1 — FAQ

| Question | Answer | Category | Keywords |
|----------|--------|----------|----------|

Populate it with your frequently asked questions.

### Sheet 2 — ChatLogs

| Timestamp | User | Question | AI Answer |

This sheet stores every chatbot interaction automatically.

---

## 📁 Repository Structure

```text
AI-FAQ-Chatbot-with-Knowledge-Base-using-n8n
│
├── workflow.json
├── README.md
├── screenshots/
│   ├── workflow.png
│   ├── execution.png
│   ├── telegram-chat.png
│   └── google-sheets.png
│
└── sample-data/
    └── FAQ_Database.xlsx
```

---

## 🎯 Skills Demonstrated

- AI Workflow Automation
- Telegram Bot Development
- Google Sheets Integration
- Knowledge Base Retrieval
- Prompt Engineering
- AI Chatbot Development
- JavaScript Data Processing
- Workflow Automation
- No-Code / Low-Code Development

---

## 🔮 Future Improvements

- Integrate Qdrant Vector Database for semantic search
- Use Ollama for fully local AI inference
- Support PDF and DOCX knowledge bases
- Add multilingual responses
- Integrate Notion as a knowledge base
- Add confidence scoring for AI responses
- Support voice questions via Telegram
- Implement human handoff for unanswered queries

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Belio Sinangote**

**30-Day n8n Automation Roadmap — Day 13 Project**

Building one portfolio-ready automation every day to master n8n, AI Automation, and Workflow Development.

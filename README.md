# 📚 AI FAQ Chatbot with Knowledge Base using n8n

An AI-powered FAQ chatbot built with **n8n**, **Google Gemini AI**, **Google Sheets**, and **Telegram**. This workflow automatically receives questions from Telegram users, retrieves relevant information from a Google Sheets knowledge base, generates accurate AI responses, logs every conversation, and replies instantly through Telegram.

Developed as part of my **30-Day n8n Automation Portfolio**, this project demonstrates how AI and workflow automation can build an intelligent knowledge base chatbot.

---

# 📌 Features

* 💬 Receives questions through Telegram
* 📚 Uses Google Sheets as a dynamic knowledge base
* 🤖 Generates AI-powered responses using Google Gemini
* 📝 Retrieves and formats FAQ data automatically
* 📊 Logs chatbot conversations to Google Sheets
* 📲 Sends instant replies through Telegram
* ⚡ Fully automated FAQ chatbot workflow

---

# 🛠 Technologies Used

* n8n
* Telegram Trigger
* Google Sheets
* Code Node (JavaScript)
* Google Gemini AI Agent
* Telegram Bot API
* Google Sheets API

---

# 📂 Workflow

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

# ⚙ Workflow Explanation

## 1. Telegram Trigger

Receives incoming questions from Telegram users.

**Captured Information**

* User
* Chat ID
* Question

---

## 2. Google Sheets

Retrieves relevant FAQ entries from the knowledge base.

**Knowledge Base Fields**

* Question
* Answer
* Category
* Keywords

---

## 3. Code Node

Formats the retrieved FAQ data into structured context before sending it to the AI Agent.

---

## 4. Google Gemini AI Agent

Analyzes the user's question together with the knowledge base and generates an accurate response.

### Example AI Response

```text
User:
Do you build n8n workflows?

AI:
Yes, we build custom n8n workflows for businesses.
```

---

## 5. Telegram

Sends the AI-generated response back to the user.

---

## 6. Google Sheets

Logs every chatbot interaction.

### Logged Information

| Timestamp | User | Question | AI Answer |
| --------- | ---- | -------- | --------- |

---

# 📁 Repository Structure

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

# 📷 Screenshots

Include the following screenshots:

* Complete Workflow
* Telegram Trigger
* Google Sheets
* Code Node
* AI Agent
* Telegram Chat
* Workflow Execution

---

# 🎯 Learning Objectives

This project demonstrates:

* Telegram Bot Automation
* Google Sheets Integration
* AI Knowledge Base Retrieval
* Prompt Engineering
* JavaScript Data Processing
* AI Chatbot Development
* Workflow Automation
* AI-Powered FAQ Systems

---

# 🚀 Possible Improvements

* Integrate Qdrant Vector Database for semantic search
* Use Ollama for fully local AI inference
* Support PDF and DOCX knowledge bases
* Add multilingual responses
* Integrate Notion as a knowledge base
* Add confidence scoring for AI responses
* Support voice questions via Telegram
* Implement human handoff for unanswered queries

---

# 📄 License

This project is licensed under the **MIT License**.

---

# 🙌 Acknowledgements

* n8n
* Google Gemini AI
* Telegram Bot API
* Google Sheets API

---

# 👨‍💻 Author

**Belio C. Sinangote**

BS Information Technology Student
Cebu Technological University (CTU)

GitHub: https://github.com/belioautomation

This project is part of my **30-Day n8n Automation Portfolio**, showcasing practical AI-powered workflow automation using n8n and Google Gemini.

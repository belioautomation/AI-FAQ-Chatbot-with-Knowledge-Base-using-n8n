# 📚 AI FAQ Chatbot with Knowledge Base — n8n Automation

An AI-powered knowledge base chatbot built using **n8n**, **Google Gemini AI**, **Google Sheets**, and **Telegram Bot API**.

This system allows users to ask questions through Telegram, retrieves relevant FAQ information from a structured Google Sheets knowledge base, generates accurate AI responses using Google Gemini, logs conversations, and provides instant automated replies.

**Stack:**  
n8n · Google Gemini AI · Telegram Bot API · Google Sheets · JavaScript · Knowledge Base Automation


---

# 🎯 Project Overview


## Problem

Organizations receive repetitive questions about:

- Products
- Services
- Processes
- Documentation
- Support information


Manually answering the same questions repeatedly reduces productivity and increases response time.


---

## Solution

This project creates an AI-powered FAQ assistant that:


1. Receives user questions through Telegram
2. Retrieves information from a knowledge base
3. Provides context to Google Gemini AI
4. Generates accurate answers
5. Sends responses automatically
6. Stores conversation history for analysis


---

# ✨ Features


## Chatbot Features

✅ Telegram-based chatbot interface  
✅ Instant AI-generated answers  
✅ Context-aware responses  
✅ Automated FAQ handling  
✅ Conversation logging  


## Knowledge Base Features

✅ Google Sheets as dynamic database  
✅ FAQ retrieval system  
✅ Structured knowledge formatting  
✅ Easy knowledge updates without changing workflow  


## AI Automation

✅ Google Gemini AI integration  
✅ AI Agent processing  
✅ Prompt-based knowledge retrieval  
✅ Automated response generation  


---

# 🗺️ System Architecture


```mermaid
flowchart TD


A["👤 Telegram User"]

--> B["📱 Telegram Trigger"]


B --> C["📚 Google Sheets Knowledge Base"]


C --> D["⚙️ Format Knowledge Context"]


D --> E["🤖 Google Gemini AI Agent"]


E --> F["📝 Generate Answer"]


F --> G["📱 Telegram Response"]


G --> H["📊 Save Chat Logs"]

````

---

# 🏗️ Workflow Implementation

# Workflow 1: AI FAQ Knowledge Base Chatbot

## Node 1 — Telegram Trigger

### Purpose

Receive questions from Telegram users.

Captured Data:

| Field     | Description              |
| --------- | ------------------------ |
| User ID   | Telegram user identifier |
| Chat ID   | Conversation ID          |
| Question  | User message             |
| Timestamp | Message time             |

Example Input:

```json
{
"user":"Belio",

"question":
"What services do you provide?"
}
```

---

# Node 2 — Google Sheets Knowledge Base

### Purpose

Retrieve stored FAQ information.

Knowledge Base Structure:

| Field    | Description          |
| -------- | -------------------- |
| Question | Common user question |
| Answer   | Expected response    |
| Category | FAQ topic            |
| Keywords | Search terms         |

Example Data:

| Question                 | Answer                           |
| ------------------------ | -------------------------------- |
| What is n8n?             | Workflow automation platform     |
| Do you build automation? | Yes, custom automation workflows |

---

# Node 3 — Code Node

### Purpose

Format FAQ data into AI-readable context.

Process:

```
Google Sheets Data

        ↓

JavaScript Formatting

        ↓

AI Context
```

Example:

```
Knowledge Base:

Q:
What is n8n?


A:
n8n is a workflow automation platform.
```

---

# Node 4 — Google Gemini AI Agent

### Purpose

Generate answers using user questions and knowledge base context.

AI Process:

1. Understand user question
2. Analyze FAQ information
3. Generate relevant response
4. Return final answer

Example:

```
User:

Do you build n8n workflows?


AI:

Yes, we create custom n8n workflows
for business automation.
```

---

# Node 5 — Telegram Response

### Purpose

Send AI-generated answers back to users.

Output:

```
Telegram User

        ▲

        |

AI Generated Response
```

---

# Node 6 — Google Sheets Chat Logs

### Purpose

Store chatbot conversations.

Logged Information:

| Field     | Description        |
| --------- | ------------------ |
| Timestamp | Conversation time  |
| User      | Telegram user      |
| Question  | User input         |
| AI Answer | Generated response |

---

# 📊 Knowledge Base Structure

Example:

| Category   | Question            | Answer                      |
| ---------- | ------------------- | --------------------------- |
| Automation | What is n8n?        | Workflow automation tool    |
| Services   | Do you create bots? | Yes, AI chatbot development |

---

# 🔐 Credentials Required

| Service       | Purpose            |
| ------------- | ------------------ |
| Telegram API  | Chat communication |
| Google OAuth2 | Sheets access      |
| Gemini API    | AI responses       |
| n8n Instance  | Workflow execution |

---

# ⚙️ Setup Guide

## 1. Create Telegram Bot

Steps:

1. Open Telegram
2. Search BotFather
3. Create new bot
4. Copy API token
5. Connect bot credential in n8n

---

## 2. Create Knowledge Base

Create Google Sheet:

```
FAQ Knowledge Base
```

Columns:

```
Question
Answer
Category
Keywords
```

Add FAQ information.

---

## 3. Configure Google Gemini

Add Gemini API credentials:

```
GOOGLE_GEMINI_API_KEY
```

Test AI response generation.

---

## 4. Import n8n Workflow

Import:

```
workflow.json
```

Configure:

* Telegram Trigger
* Google Sheets credential
* Gemini AI Agent

Activate workflow.

---

# 🧪 Testing Checklist

| Test Case               | Expected Result          |
| ----------------------- | ------------------------ |
| Send Telegram question  | Workflow starts          |
| FAQ exists              | Correct answer generated |
| Gemini receives context | AI response created      |
| Telegram reply sent     | User receives answer     |
| Chat log saved          | Conversation stored      |

---

# 📁 Repository Structure

```
AI-FAQ-Chatbot-with-Knowledge-Base-using-n8n/

│
├── README.md
│
├── workflow.json
│
├── screenshots/
│   │
│   ├── workflow.png
│   ├── telegram-trigger.png
│   ├── google-sheets.png
│   ├── code-node.png
│   ├── ai-agent.png
│   ├── telegram-chat.png
│   └── execution-result.png
│
└── sample-data/
    │
    └── FAQ_Database.xlsx
```

---

# 📸 Screenshots

Recommended screenshots:

* Complete workflow
* Telegram Trigger
* Knowledge Base Sheet
* Code Node formatting
* Gemini AI Agent
* Telegram conversation
* Chat logs
* Workflow execution

---

# 🚀 Future Improvements

| Feature                 | Implementation                     |
| ----------------------- | ---------------------------------- |
| Vector Search           | Qdrant/Pinecone semantic retrieval |
| Local AI                | Ollama deployment                  |
| Document Knowledge Base | PDF/DOCX processing                |
| Better Search           | Embedding-based retrieval          |
| Confidence Score        | AI answer validation               |
| Voice Support           | Speech-to-text integration         |
| Human Handoff           | Transfer unanswered questions      |
| Analytics Dashboard     | Chat performance tracking          |
| Multi-language          | Language detection                 |

---

# 🎓 Skills Applied

## Automation

* n8n Workflow Automation
* Event-driven chatbot systems
* Knowledge workflow design

## Artificial Intelligence

* Google Gemini AI
* AI Agent Development
* Prompt Engineering
* Knowledge-based AI responses

## Programming

* JavaScript
* Data formatting
* Workflow logic

## APIs

* Telegram Bot API
* Google Sheets API
* Gemini AI API

---

# 📚 Learning Objectives

This project demonstrates:

* Building AI knowledge base systems
* Creating chatbot workflows
* Integrating LLMs with external data
* Designing automated support assistants
* Managing conversational data

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

GitHub:

[https://github.com/belioautomation](https://github.com/belioautomation)

This project is part of my **30-Day n8n Automation Portfolio**, showcasing AI-powered workflow automation using n8n, Google Gemini AI, APIs, and intelligent chatbot systems.

---

# 📄 License

MIT License

```

This now aligns with your other projects and positions it as an **AI Knowledge Base / RAG-style chatbot automation project**, which is a stronger portfolio category than a simple FAQ bot.
```

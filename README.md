# 📚 AI FAQ Chatbot with Knowledge Base — n8n Automation

![n8n](https://img.shields.io/badge/n8n-Automation-orange)
![Google Gemini](https://img.shields.io/badge/AI-Google%20Gemini-blue)
![Telegram](https://img.shields.io/badge/API-Telegram-green)
![JavaScript](https://img.shields.io/badge/Code-JavaScript-yellow)
![License](https://img.shields.io/badge/license-MIT-green)

An AI-powered knowledge base chatbot workflow built using **n8n**, **Google Gemini AI**, **Google Sheets**, and **Telegram Bot API**.

This system allows users to ask questions through Telegram, retrieves relevant information from a structured FAQ knowledge base, provides context to Google Gemini AI, generates accurate responses, logs conversations, and delivers instant automated answers.

**Stack:**  
n8n · Google Gemini AI · Telegram Bot API · Google Sheets · JavaScript · Knowledge Base Automation · AI Agent


---

# 🎯 Project Overview


## Problem

Organizations receive repetitive questions about:


- Products
- Services
- Documentation
- Internal processes
- Technical information
- Frequently asked questions


Manually answering the same questions repeatedly creates several challenges:


- Increased support workload
- Slow response times
- Repetitive manual tasks
- Inconsistent answers
- Limited availability outside working hours


Common use cases:


- Customer support assistants
- Internal company assistants
- Product information bots
- Documentation helpers


---

## Solution

This project creates an AI-powered FAQ assistant that automatically:


1. Receives user questions through Telegram
2. Retrieves relevant information from a knowledge base
3. Formats FAQ data into AI-readable context
4. Sends context and user questions to Google Gemini AI
5. Generates accurate responses
6. Sends answers back through Telegram
7. Stores conversation history for analysis


The workflow acts as an intelligent knowledge assistant capable of answering questions using stored organizational information.


---

# ✨ Features


## Chatbot Features

✅ Telegram chatbot interface  
✅ Instant AI-generated responses  
✅ Natural language understanding  
✅ Context-aware answers  
✅ Automated FAQ handling  
✅ Conversation logging  


## Knowledge Base Features

✅ Google Sheets knowledge database  
✅ Dynamic FAQ management  
✅ Structured information storage  
✅ Easy knowledge updates  
✅ External data integration  


## Artificial Intelligence

✅ Google Gemini AI integration  
✅ AI Agent processing  
✅ Knowledge-based response generation  
✅ Prompt engineering workflow  
✅ Context-aware AI answers  


## Automation

✅ n8n workflow automation  
✅ Automated chatbot pipeline  
✅ Real-time message processing  
✅ API-based integrations  


---

# 🗺️ System Architecture


```mermaid
flowchart TD


A["👤 Telegram User"]

--> B["📱 Telegram Trigger"]


B --> C["📚 Google Sheets Knowledge Base"]


C --> D["⚙️ JavaScript Context Formatter"]


D --> E["🤖 Google Gemini AI Agent"]


E --> F["📝 Generate AI Response"]


F --> G["📱 Telegram Response"]


G --> H["📊 Save Chat Logs"]

````

---

# 🏗️ Workflow Implementation

# Workflow 1: AI FAQ Knowledge Base Chatbot

## Node 1 — Telegram Trigger

### Purpose

Receive questions from users through Telegram and start the chatbot workflow.

Captured Information:

| Field     | Description              |
| --------- | ------------------------ |
| User ID   | Telegram user identifier |
| Chat ID   | Conversation identifier  |
| Question  | User message             |
| Timestamp | Message received time    |

Example Input:

```json
{
"user":
"Belio",

"question":
"What services do you provide?",

"chat_id":
"123456789"
}
```

---

# Node 2 — Google Sheets Knowledge Base

### Purpose

Retrieve FAQ information that will be used as AI knowledge context.

Knowledge Base Structure:

| Field    | Description          |
| -------- | -------------------- |
| Question | Common user question |
| Answer   | Expected response    |
| Category | FAQ topic            |
| Keywords | Search terms         |

Example Data:

| Question            | Answer                       | Category   |
| ------------------- | ---------------------------- | ---------- |
| What is n8n?        | Workflow automation platform | Automation |
| Do you create bots? | Yes, AI chatbot development  | Services   |

The knowledge base can be updated without modifying the n8n workflow.

---

# Node 3 — Code Node (Knowledge Formatter)

### Purpose

Transform Google Sheets data into structured context for Gemini AI.

Processing:

```text
Google Sheets Data

        ↓

JavaScript Formatting

        ↓

AI Knowledge Context
```

Example Output:

```text
Knowledge Base:


Question:

What is n8n?


Answer:

n8n is a workflow automation platform
that connects APIs and applications.
```

---

# Node 4 — Google Gemini AI Agent

### Purpose

Generate accurate responses using user questions combined with knowledge base information.

AI Process:

1. Understand user question
2. Analyze provided knowledge
3. Match relevant information
4. Generate final response

Example:

```text
User:

Do you build automation workflows?


AI:

Yes, we create custom n8n automation
workflows for different business needs.
```

AI Capabilities:

* Question answering
* Context analysis
* Knowledge retrieval
* Natural language generation

---

# Node 5 — Telegram Response

### Purpose

Send AI-generated answers back to Telegram users.

Response Flow:

```text
AI Generated Response

          ↓

Telegram Bot API

          ↓

User Receives Answer
```

Example:

```text
User:

What is n8n?


AI:

n8n is a workflow automation platform
that connects applications and APIs.
```

---

# Node 6 — Google Sheets Chat Logs

### Purpose

Store chatbot conversations for monitoring and analysis.

Logged Information:

| Field     | Description        |
| --------- | ------------------ |
| Timestamp | Conversation time  |
| User      | Telegram user      |
| Question  | User input         |
| AI Answer | Generated response |

Example:

| User  | Question     | Answer                          |
| ----- | ------------ | ------------------------------- |
| Belio | What is n8n? | Automation platform explanation |

---

# 📊 Knowledge Base Structure

Example:

| Category   | Question                   | Answer                   |
| ---------- | -------------------------- | ------------------------ |
| Automation | What is n8n?               | Workflow automation tool |
| Services   | Do you create bots?        | AI chatbot development   |
| Support    | How can I contact support? | Contact information      |

The knowledge base acts as the chatbot's external information source.

---

# 🔐 Credentials Required

| Service           | Purpose                |
| ----------------- | ---------------------- |
| Telegram Bot API  | User communication     |
| Google OAuth2     | Google Sheets access   |
| Google Gemini API | AI response generation |
| n8n Instance      | Workflow execution     |

---

# ⚙️ Setup Guide

## 1. Create Telegram Bot

Steps:

1. Open Telegram
2. Search BotFather
3. Create a new bot
4. Copy API token
5. Add Telegram credentials in n8n

Test incoming messages.

---

## 2. Create Knowledge Base

Create Google Sheet:

```text
FAQ Knowledge Base
```

Required columns:

```text
Question

Answer

Category

Keywords
```

Add FAQ information.

---

## 3. Configure Google Gemini AI

Add Gemini credentials:

```text
GOOGLE_GEMINI_API_KEY
```

Test AI response generation.

---

## 4. Configure Chat Logs

Create Google Sheet:

```text
Chat History
```

Columns:

```text
Timestamp

User

Question

AI Answer
```

---

## 5. Import n8n Workflow

Import:

```text
workflow.json
```

Configure:

* Telegram Trigger
* Google Sheets credential
* Gemini AI Agent
* Telegram Response node

Activate workflow.

---

# 🧪 Testing Checklist

| Test Case               | Expected Result        |
| ----------------------- | ---------------------- |
| Send Telegram question  | Workflow starts        |
| Knowledge base loads    | FAQ data retrieved     |
| Context formatter runs  | AI context created     |
| Gemini receives context | Answer generated       |
| Telegram reply sent     | User receives response |
| Chat logs saved         | Conversation stored    |

---

# 📁 Repository Structure

```text
AI-FAQ-Chatbot-with-Knowledge-Base-n8n/

│
├── README.md
│
├── workflow.json
│
├── screenshots/
│   │
│   ├── workflow.png
│   ├── telegram-trigger.png
│   ├── google-sheets-knowledge-base.png
│   ├── code-node-context.png
│   ├── gemini-ai-agent.png
│   ├── telegram-response.png
│   ├── chat-logs.png
│   └── execution-result.png
│
└── sample-data/
    │
    └── FAQ_Database.xlsx
```

---

# 📸 Screenshots

Recommended screenshots:

* Complete n8n workflow
* Telegram Trigger configuration
* Knowledge Base Google Sheet
* Context formatting output
* Gemini AI Agent setup
* Telegram conversation result
* Chat log database
* Workflow execution result

---

# 🚀 Future Improvements

| Feature                 | Implementation                     |
| ----------------------- | ---------------------------------- |
| Vector Search           | Qdrant/Pinecone semantic retrieval |
| RAG Pipeline            | Embedding-based knowledge search   |
| Local AI                | Ollama deployment                  |
| Document Knowledge Base | PDF/DOCX processing                |
| Confidence Score        | AI answer validation               |
| Voice Support           | Speech-to-text integration         |
| Human Handoff           | Transfer unanswered questions      |
| Analytics Dashboard     | Chat performance tracking          |
| Multi-language Support  | Language detection                 |

---

# 🎓 Skills Applied

## Automation

* n8n Workflow Automation
* Event-driven chatbot systems
* Knowledge workflow design
* API integration

## Artificial Intelligence

* Google Gemini AI
* AI Agent Development
* Prompt Engineering
* Knowledge-based AI responses
* Context-aware generation

## Programming

* JavaScript
* Data formatting
* JSON processing
* Workflow logic

## APIs

* Telegram Bot API
* Google Sheets API
* Gemini AI API

## Business Automation

* AI support assistants
* Knowledge management automation
* Customer communication systems

---

# 📚 Learning Objectives

This project demonstrates:

* Building AI-powered knowledge systems
* Creating chatbot automation workflows
* Integrating LLMs with external data sources
* Designing FAQ assistants
* Managing conversational information
* Developing practical AI automation solutions

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

This project is part of my **30-Day n8n Automation Portfolio**, showcasing AI-powered workflow automation using **n8n, Google Gemini AI, APIs, and intelligent knowledge-based chatbot systems**.

---

# 📄 License

MIT License

```
```

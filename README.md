# N8N-resturant-chatbot-with-ai-automation
🤖 WhatsApp AI Agent with Memory (n8n)

A production-ready WhatsApp AI chatbot built using n8n, Google Gemini, and Simple Memory, capable of handling multi-turn conversations and persisting data in Google Sheets without manual workflow execution.

🚀 Features

📲 WhatsApp-based chat interface

🧠 Persistent conversation memory (multi-turn chat)

🤖 AI-powered responses using Google Gemini

📊 Read & write data to Google Sheets

🔁 Fully automated (no manual “Execute Workflow” needed)

⚡ Scalable and production-ready architecture

🛠 Tech Stack

n8n – Workflow automation

WhatsApp Cloud API – Message trigger & response

Google Gemini Chat Model – AI responses

Simple Memory (n8n) – Conversation memory

Google Sheets – Database & order logging

📐 Workflow Architecture
WhatsApp Trigger
      ↓
   AI Agent
   ├── Google Gemini (Chat Model)
   ├── Simple Memory (Session-based)
   ├── Google Sheets (Read: database)
   └── Google Sheets (Append: order list)
      ↓
WhatsApp Send Message

🧠 Memory Configuration (IMPORTANT)

To enable continuous chat without re-running the workflow:

Simple Memory Node Settings

Session ID: Connected Chat Trigger

Key: (Leave empty)

Context Window Length: 10–20

This ensures:

Same user → same memory

Multiple messages → preserved context

▶️ How It Works

User sends a message on WhatsApp

WhatsApp Trigger activates the workflow

AI Agent processes the message using:

Chat Model (Gemini)

Memory (conversation context)

Google Sheets (data lookup/storage)

Response is sent back to WhatsApp

User can continue chatting naturally (2–3+ messages)

⚙️ Setup Instructions
1️⃣ Clone the Repository
git clone https://github.com/your-username/whatsapp-ai-agent-n8n.git

2️⃣ Import Workflow into n8n

Open n8n

Go to Workflows → Import

Upload the workflow JSON file

3️⃣ Configure Credentials

WhatsApp Cloud API credentials

Google Gemini API key

Google Sheets OAuth credentials

4️⃣ Activate the Workflow

⚠️ Critical Step

Click Activate (top-right corner of n8n)

❌ Do NOT use “Execute Workflow” for chatting

✅ Send messages directly from WhatsApp

🧪 Testing

Activate workflow

Send WhatsApp message:

Hi


Follow up:

What did I just say?


Bot should respond correctly using memory

🛑 Common Issues & Fixes
❌ “Key parameter is empty” (Simple Memory)

✔ Use Connected Chat Trigger
✔ Leave Key empty

❌ Have to click Execute every time

✔ Workflow must be Active, not executed manually

📌 Use Cases

Customer support chatbot

Order management system

Subscription tracker

Lead qualification bot

Personal AI assistant on WhatsApp

🔒 Production Notes

Enable execution logging if needed

Add rate-limiting for public bots

Secure API keys using environment variables

Set up an error workflow in n8n

📄 License

MIT License – free to use, modify, and distribute.

🙌 Acknowledgements

n8n

Google Gemini

WhatsApp Cloud API

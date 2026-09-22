# 🏥 Patient Medication Reminder & Compliance System

An enterprise-grade, automated healthcare workflow built with **n8n**, **Supabase**, **Telegram Bot API**, and **OpenAI (Advanced AI Agent)**. This end-to-end system automates patient medication scheduling, captures real-time interactive compliance feedback, logs health adherence data, and delivers empathetic, AI-driven responses.

---

## 🏗️ System Architecture & Workflow Flow

The workflow is designed with a robust, decoupled dual-loop architecture:

1. **Outbound Dispatch Loop (Reminders):**
   * **Schedule Trigger:** Automatically initiates the cycle at scheduled intervals.
   * **Supabase Nodes:** Securely retrieves active patient profiles and medication schedules from the database.
   * **Telegram Node:** Dispatches rich-text reminder notifications equipped with interactive inline buttons (**Taken ✅** / **Snooze ⏰**).

2. **Inbound Compliance & AI Feedback Loop:**
   * **Telegram Trigger (`callback_query`):** Listens for real-time patient interactions from the Telegram buttons.
   * **Conditional Logic (If Node):** Evaluates user choices (`TAKEN` vs `SNOOZE`).
   * **Database Logging (Supabase):** Logs the patient's adherence status directly into the `reminder_logs` table.
   * **AI Agent Engine (OpenAI GPT):** Processes the status and generates contextual, warm, and encouraging Arabic/multilingual replies.
   * **Confirmation Dispatch:** Delivers the personalized feedback back to the patient via Telegram.

---

## 🛠️ Tech Stack

* **Workflow Automation:** n8n
* **Database & Backend:** Supabase (PostgreSQL)
* **Messaging Interface:** Telegram Bot API
* **Artificial Intelligence:** OpenAI Chat Models via n8n Advanced AI nodes

---

## 🚀 Key Features

* **End-to-End Automation:** Seamless zero-touch scheduling and real-time response handling.
* **Interactive UX:** Frictionless patient engagement using Telegram callback buttons.
* **Generative AI Integration:** Empathetic, context-aware conversational feedback enforcing tailored health responses.
* **Robust Auditing:** Clean data logging schema tracking patient compliance history.

---

## ⚙️ Setup & Deployment

1. Import the workflow JSON into your n8n instance.
2. Configure your credentials for **Supabase**, **Telegram Bot API**, and **OpenAI**.
3. Set up your Supabase tables (`patients`, `medication_schedule`, `reminder_logs`).
4. Activate the workflow and test the interactive loop!

   ---

   ## Workflow
   <img width="1920" height="866" alt="image" src="https://github.com/user-attachments/assets/f2984e0f-bf95-4eef-9517-458aa0ee566b" />

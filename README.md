# AI Automation Hub: Personal Utility Workflows

This repository contains a collection of **agentic workflows** built on [n8n](https://n8n.io/). These projects focus on practical AI applications, featuring **Generator-Evaluator loops**, **multi-model redundancy**, and **structured data extraction**.

---

## 🛠 Featured Workflows

### 1. Polyglot Daily: Multilingual Learning Architect
An automated tutor that manages vocabulary acquisition across English, Kannada, Japanese, and Korean.
* **Logic**: Interrogates an n8n Data Table to retrieve historical data, ensuring the AI does not repeat previously taught words.
* **Agentic Pattern**: Features a dual-agent structure: a **Tutor Agent** for content generation and a **Parser Agent** to structure output for database insertion.
* **Tech**: n8n Data Tables, Groq (GPT-OSS), JavaScript, Gmail API.



### 2. Context-Aware Weather & Gear Guide
A reasoning-based automation that translates meteorological data into actionable daily advice.
* **Logic**: Fetches live data from the NOAA API and utilizes an LLM to interpret weather "feel" rather than just raw temperature.
* **Intelligence**: Provides specific clothing recommendations for a one-hour departure window.
* **Tech**: NOAA Weather API, Groq (Llama-3), n8n Markdown/HTML engine.

### 3. Food for Thought: Culinary Theory Auditor
A high-fidelity feedback loop for recipe development based on Michelin-star principles.
* **Agentic Pattern**: Implements a **Generator-Evaluator loop** where a "Chef Agent" drafts a critique and a "QA Agent" audits it against a strict 5-point binary rubric.
* **Architecture**: Utilizes a multi-model fallback strategy between Groq and Google Gemini to ensure high availability.
* **Tech**: n8n Forms, Google Gemini, Groq, Resend API.



---

## ⚙️ Prerequisites

| Workflow | System Requirements | Required Credentials |
| :--- | :--- | :--- |
| **Polyglot** | n8n Data Table (`vocabulary_store_id`) | Groq, Gmail OAuth2 |
| **Weather** | User-Agent Header config | Groq, Gmail OAuth2 |
| **Culinary** | Public n8n URL (for Form submissions) | Groq, Gemini, Resend |

---

## 🚀 Deployment
1. Download the `.json` files from the `/workflows` directory.
2. In n8n, click **Import from File** to upload the canvas.
3. Configure your respective API keys in the highlighted credential nodes.

---

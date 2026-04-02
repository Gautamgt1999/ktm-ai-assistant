# ktm-ai-assistant
A multi-agent Generative AI assistant for KTM Duke 200 maintenance and parts. Built with Dialogflow CX, utilizing RAG (Retrieval-Augmented Generation) for technical manual queries and BigQuery integration for real-time spare parts data.
# KTM Duke 200 AI Assistant: Multi-Agent RAG System 🏍️

An advanced Generative AI assistant built on **Google Cloud Platform** to support KTM Duke 200 owners with technical maintenance and genuine parts procurement.

---
🚀 Live Demo: https://ktm-ai-assistant.tiiny.site

## 📌 The Problem
Maintaining a high-performance motorcycle like the KTM Duke 200 (BS3/BS4/BS6) requires precision. Owners often struggle with:
* **Technical Information Overload:** Sifting through 200+ page service manuals for specific torque specs or fluid capacities.
* **Parts Accuracy:** Finding correct part numbers and real-time pricing without visiting a dealership.
* **Safety Risks:** Performing DIY repairs without proper safety warnings or professional-grade guidance.

## 🛠️ The Tech Stack
This project leverages the full **Google Cloud Generative AI** ecosystem:
* **Dialogflow CX:** For conversational design and multi-agent orchestration.
* **Vertex AI Search & Conversation:** Powering the RAG (Retrieval-Augmented Generation) engine.
* **BigQuery:** Hosting the structured "Spare Parts & Pricing" database.
* **Cloud Storage:** Storing unstructured technical manuals (PDFs).
* **Gemini 1.5 Flash:** The core LLM driving reasoning and safety-aware responses.

## 🤖 Intelligent Multi-Agent Architecture
The system uses a **Primary-Subordinate Agent** design to ensure expert-level responses:

### 1. The Master Tech Agent (Technical Expert)
* **Role:** Specialized in mechanical diagnostics and repair steps.
* **Data Source:** Unstructured RAG (Official 200 Duke Service Manual).
* **Key Feature:** Automatically triggers **Safety Warnings** for high-risk tasks (brakes, engine, electrical).

### 2. The Parts Specialist Agent (Data Expert)
* **Role:** Handles pricing, part numbers, and stock availability.
* **Data Source:** Structured SQL queries via BigQuery.
* **Handoff Logic:** If a user asks the Master Tech "How much does the oil filter cost?", the system seamlessly routes the query to the Parts Specialist without losing context.

## 🚀 Key Features
* **Grounding:** All answers are grounded in official documentation to prevent "AI Hallucinations."
* **Dynamic Pricing:** Real-time part price retrieval in INR.
* **Safety-First Design:** Mandatory cool-down and stand-stability checks before technical instructions.

---

### 📂 Repository Structure
* `agent-config/`: Contains the exported Dialogflow CX JSON for local testing/importing.
* `data-samples/`: Sample structure of the BigQuery parts table and PDF snippets.
* ## 📸 Project Architecture Preview
| Multi-Agent Playbooks | RAG & Database Tools |
|---|---|


---
*Created by [Gautam Thiruvalluvan](https://linkedin.com/in/your-profile-link) as part of the Google Cloud Gen AI Academy.*

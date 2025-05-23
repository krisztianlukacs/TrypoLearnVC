# Product & Tech Stack

# **🧪 Product & Tech Stack**

## **🧰 1. Product Overview (MVP)**

The current MVP is a web-based AI learning assistant that allows users to:

- 📄 **Upload university documents** (slides, notes, PDFs)
- 💬 **Ask natural language questions** about the content
- 📚 **Receive answers grounded in those documents** using RAG
- 🧑‍🤝‍🧑 **Invite classmates to study together** on shared documents (admin only)
- ❓ **Log unanswered questions** to improve the model over time
- 📝 **Generate exam questions and study quizzes** based on the syllabus

### **📸 Sample Features (available in MVP)**

- Document-based chat (Notion-style UI)
- Group access with shared chat history (in progress)
- Smart tagging of learning objectives and key concepts
- Question generator from syllabus PDFs
- Feedback system on AI answers (unanswered questions, and logging)

---

## **⚙️ 2. Architecture & AI Stack**

### **📦 Core Architecture**

**Retrieval-Augmented Generation (RAG)**:

- Documents are embedded & stored in a vector database
- When a user asks a question, the system:
    1. Retrieves the most relevant context (e.g. lecture slide excerpts)
    2. Feeds that context into a Large Language Model (e.g. GPT-4)
    3. Generates an answer grounded in retrieved content

### **🧠 Technologies Used**

| **Layer** | **Stack** |
| --- | --- |
| Frontend | Angular,CSS |
| Backend | Php, BigQuery |
| AI/LLM | OpenAI API (GPT-4) |
| Vector DB | GCP |
| Embeddings | OpenAI and Gemini |
| Middleware | LangChain for RAG logic |
| Storage | GCP BigQuery, GCP Datastore |
| Hosting | GCP App Engine |

---

## **👩‍💻 3. UX Principles**

- 🧠 **Familiarity**: Built to feel intuitive, like Notion or Google Docs
- ⚡ **Speed**: Answers delivered in <5s with real-time document context
- 📲 **Cross-platform**: Fully responsive, mobile-friendly MVP
- 🤝 **Collaborative**: Real-time learning with shared AI sessions
- 📚 **Academic grounding**: Always sourced from validated course content

---

## **📈 4. System in Action**

1. **Upload** your semester’s syllabus and lecture slides
2. **Chat** with your materials like they’re a tutor
3. **Invite friends** to join the same workspace (Admin only)
4. **Save/Tag/Export** key concepts and exam answers
5. **Improve** the system with community Q&A loop
6. **Admin** can manage user access and permissions
7. **Telegram** can answer via Telegram bot

---

## **🧪 MVP Status**

- ✅ Live with over 1000 real student users
- ✅ Integrated into 2 institutional learning environments
- ✅ MVP supports multiple users per doc, tracked sessions, and versioning
- 🔜 In development: instructor dashboards, analytics, LMS integration

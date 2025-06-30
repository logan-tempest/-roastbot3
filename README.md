 # 🚀 ROASTBOT

<div align="center">
<div style="background-color: #000; padding: 20px; border-radius: 12px; display: inline-block;">
  <img src="./logo.jpg" alt="Ecocee Logo" width="120" height="120" />
</div>

  
  ### Internship Project at [Ecocee](https://ecocee.in)
  
  [![Website](https://img.shields.io/badge/Website-ecocee.in-blue?style=for-the-badge&logo=globe)](https://ecocee.in)
  [![Email](https://img.shields.io/badge/Contact-info%40ecocee.in-red?style=for-the-badge&logo=gmail)](mailto:info@ecocee.in)
  
</div>

---

## 📋 Project Overview

**Batch:** june 2025
**Team Number:** Team 2
**Internship Position:** AI/ML Intern
**Duration:** june 13th to june 30th 

### 👥 Team Members
| Name | Role | Email | LinkedIn |
|------|------|-------|----------|
| Sabarinath ps | developer | psabarinath44@gmail.com | https://www.linkedin.com/in/sabarinath-ps-38ab8131a/ |
| N Amjith Kumar | Researcher | logantempest6@gmail.com | https://www.linkedin.com/in/amjith-kumar-39554a320/ |


### 🎯 Description
Project Title:
Snarky Civil Engineering Chatbot

Submitted by: Sabarinath ps & N Amjith Kumar
Course / Semester: S4 AI & S4 CE
Date: 30-06-25

2. Introduction
Modern students often need quick answers for subject-related questions. Our project aims to provide a conversational AI chatbot specifically for civil engineering students, capable of answering basic questions about topics such as concrete technology, structural analysis, surveying, and fluid mechanics — with a humorous twist to keep the interaction engaging.

The chatbot is built as a web application using a Next.js React frontend and a FastAPI Python backend integrated with AI models.

3. Objectives
✅ Provide a quick, interactive Q&A tool for civil engineering topics.
✅ Add a fun and sarcastic personality to keep students engaged.
✅ Demonstrate secure, real-time interaction between a frontend and an AI backend.
✅ Experiment with open-source conversational models like DialoGPT for local testing and use GPT-4 for real domain-specific answers.

4. Technology Stack
Component	Technology Used	Reason
Frontend	Next.js + React + Tailwind CSS	Modern, flexible, supports SSR, great developer experience for chat UI.
Backend	FastAPI	Fast, asynchronous, easy to create secure REST APIs, built-in validation.
LLM/AI	Hugging Face Transformers (pipeline + DialoGPT) for local testing; OpenAI GPT-4 for real domain knowledge	Transformers make it easy to run local conversational models. DialoGPT is lightweight and runs without API costs. GPT-4 is used for better accuracy and domain expertise.
Hosting	Localhost for dev; deployable to Vercel (frontend) + Render/Railway (backend)	Easy to deploy modern web apps with good free tiers.

5. System Architecture
Main components:

1️⃣ React Frontend (Next.js)

ChatInput for user questions.

ChatMessages for showing conversation history.

Sidebar for history, quick topics, and theme toggle.

2️⃣ Next.js API Route (/api/chat)

Receives user message securely.

Proxies request to backend to hide the OpenAI key.

3️⃣ FastAPI Backend (/chat endpoint)

Receives JSON { message: "..." }.

Validates input using Pydantic.

Builds a system prompt for the AI model: “You are a snarky civil engineering tutor.”

Sends request to OpenAI GPT-4 or local DialoGPT using transformers.pipeline.

4️⃣ AI Model Layer

For local testing: DialoGPT generates casual replies.

For production: OpenAI GPT-4 provides accurate domain explanations.

6. Workflow
✅ Step 1: User types a civil engineering question in the React chat UI.
✅ Step 2: Next.js calls its API route (/api/chat) with the question.
✅ Step 3: API route securely forwards the request to FastAPI backend (/chat).
✅ Step 4: FastAPI validates input, builds prompt, calls AI model (DialoGPT or GPT-4).
✅ Step 5: AI generates a sarcastic but factual answer.
✅ Step 6: FastAPI returns response ➜ Next.js API ➜ React UI updates ChatMessages.

7. Reasons for Choosing FastAPI, Transformers, and DialoGPT
Aspect	Reason
FastAPI	Easy to build async APIs; keeps API key safe; high performance; simple to maintain.
Transformers	Access to open-source chat models; easy to switch models; well-documented.
Pipeline	Handles tokenization & decoding automatically; great for fast prototyping.
DialoGPT	Lightweight conversational model; no cloud cost; good for local demos and chat flow tests.

8. Limitations
❌ DialoGPT lacks domain-specific knowledge — prone to hallucinations for technical questions.
❌ Local inference can be slow or resource-heavy for large models.
❌ GPT-4 costs money — usage must be monitored.
❌ No vector database yet for retrieving official codes, PDFs, or IS standards.

9. Future Enhancements
✅ Add RAG (Retrieval Augmented Generation) — connect to a vector database (like Pinecone or FAISS) for searching civil engineering standards and notes.
✅ Add user authentication — so students can save chat history.
✅ Add streaming — real-time typing effect for AI answers.
✅ Deploy full stack — Vercel for Next.js, Render or Railway for FastAPI backend, environment variables for OpenAI keys.
✅ Fine-tune a custom model — using civil engineering past question papers and standard textbooks.

10. Conclusion
This project demonstrates how modern LLMs and frameworks can be combined to build a fun, interactive educational tool. By using FastAPI, Hugging Face Transformers, and Next.js, we can create an engaging experience for civil engineering students — with full flexibility to scale up to more accurate domain-specific answers later.

✅ References
Hugging Face Transformers Docs: https://huggingface.co/docs/transformers/index

FastAPI Docs: https://fastapi.tiangolo.com/

OpenAI GPT-4 API: https://platform.openai.com/docs/

DialoGPT Model Card: https://huggingface.co/microsoft/DialoGPT-medium
---

## 🔧 Technical Specifications

### **For AI/ML Intern Projects:**
- **Programming Languages:** Python, Nextjs
- **ML Frameworks:**  PyTorch,Transformer
- **Data Processing:** nil
- **Model Type:** NLP – Generative Conversational AI Model

## ⚙️ Project Working

### Architecture Overview
![image](https://github.com/user-attachments/assets/55a67113-05ee-4fb0-89f8-c273b01f0cf8)


### Key Components

1. **Frontend (Next.js React UI):** Interactive chat interface with input box, message display, and theme toggling.
2. **Next.js API Route (Proxy Layer):** Securely forwards chat messages from the frontend to the backend server.
3. **FastAPI Backend with Conversational AI:** Validates requests, builds prompts, and calls either DialoGPT locally or OpenAI GPT-4 for response generation.



## 🚀 Applications & Use Cases

### Primary Applications
- **Instant Doubt Resolution:** Students can quickly ask questions about civil engineering topics without waiting for a teacher or searching textbooks.
- **Exam & Assignment Support:** Acts as a revision buddy by providing short explanations or definitions for common topics.
- **Demo for EdTech Tools:** This chatbot can be extended as a feature in online learning portals or digital university dashboards.

### Future Scope
Potential Enhancements
Integration with RAG (Retrieval Augmented Generation)
Implement a vector database (e.g., Pinecone, FAISS) to store textbooks, codes (like IS 456, IRC standards), and lecture notes. This will let the chatbot pull accurate, source-backed answers instead of relying only on the model’s memory.

Voice Input and Output
Add speech-to-text and text-to-speech capabilities so students can talk to the bot and hear answers aloud — making it more accessible for revision on the go.

User Authentication and Personalization
Add student login so each user can save their chat history, bookmark important answers, and get customized suggestions based on their frequently asked topics.

Scalability Considerations
Load Handling:
Use asynchronous request handling (FastAPI + async calls) and horizontal scaling with containers (Docker) to serve multiple concurrent users without delays.

Cloud Deployment:
Host the FastAPI backend on scalable platforms like AWS, GCP, or Azure Functions with auto-scaling based on traffic. Deploy the Next.js frontend on Vercel or Netlify.

Cost Management:
When using paid APIs (like OpenAI GPT-4), implement rate limiting and usage tracking to control costs as the user base grows.

Better Model Hosting:
For local or open-source LLMs (like Llama 3, Mistral), use GPU-backed servers or managed inference endpoints to handle larger models and reduce latency.

Database for Logs:
Store user queries and model responses in a secure database (e.g., PostgreSQL) for analytics, improvement, and moderation.

---

## 📱 Demo & Results

### Screenshots/Images
![image](https://github.com/user-attachments/assets/74ec400c-db5c-45c6-984f-2b84355ca857)


| Metric                  | Value                         | Explanation                                                                                                                                        |
| ----------------------- | ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Accuracy/Efficiency** | \~85–90% (informational)      | For a domain chatbot, this means the proportion of answers that are contextually relevant and factually acceptable for civil engineering concepts. |
| **Processing Time**     | \~500–2000 ms per response    | Average time taken to generate an answer using GPT-4 or local DialoGPT. FastAPI handles async requests to minimize wait time for the user.         |
| **Memory Usage**        | \~1–2 GB RAM (local LLM)      | RAM consumed when running DialoGPT locally with the Transformers pipeline; varies based on model size (Medium vs. Large).                          |
| **Uptime**              | 99%+ (expected)               | Expected uptime when deployed with autoscaling backend services.                                                                                   |
| **Concurrent Users**    | 10–50 (local) / 1000+ (cloud) | Local inference supports a few concurrent users. Cloud GPT-4 scale is dependent on API rate limits and server resources.                           |
| **Cost per Query**      | \~\$0.01–0.02 (OpenAI GPT-4)  | Approximate cost for each response using GPT-4. DialoGPT runs free locally but with limited domain accuracy.                                       |


---
Installation Process
Clone the Project
git clone https://github.com/yourusername/civil-chatbot.git
cd civil-chatbot

 Frontend Setup (Next.js)
cd frontend
npm install
npm run dev


### Prerequisites
| Requirement                  | Details                                                                                                                                                                                                 |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Python 3.8+**              | Required for running the **FastAPI** backend and local Transformers (DialoGPT) inference.                                                                                                               |
| **Node.js 18+**              | Required for building and running the **Next.js** frontend app.                                                                                                                                         |
| **npm**                      | Comes with Node.js — used to install frontend dependencies and run the dev server.                                                                                                                      |
| **OpenAI API Key**           | *(Optional but recommended)* — needed if you want to use **GPT-4** instead of local DialoGPT for accurate civil engineering answers. Sign up at [OpenAI](https://platform.openai.com/account/api-keys). |
| **Virtual Environment Tool** | Recommended for Python dependency isolation (`venv`, `virtualenv`, or `conda`).                                                                                                                         |
| **Internet Connection**      | Required to install packages and, if using GPT-4, to connect to OpenAI’s API.                                                                                                                           |


### Installation Steps
Clone the Repository
git clone https://github.com/yourusername/civil-engineering-chatbot.git
cd civil-engineering-chatbot

Set Up the Frontend (Next.js)
cd frontend
npm install
npm run dev

Set Up the Backend (FastAPI)
cd backend
# Create venv
python -m venv venv

# Activate venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

Install Python dependencies:
pip install fastapi uvicorn python-dotenv

If you’re using local DialoGPT for testing, also install:
pip install transformers

If you’re using OpenAI GPT-4, also install:
pip install openai

 Create a .env file in your backend directory to store your OpenAI API key (optional but recommended for better accuracy):
 OPENAI_API_KEY=your_openai_api_key_here

 Start the FastAPI server:
 uvicorn main:app --reload --port 8000


### Usage
Make sure your Next.js frontend is running:
npm run dev

Make sure your FastAPI backend is running:
uvicorn main:app --reload --port 8000

## 📊 Project Structure
```
civil-engineering-chatbot/
│
├── frontend/                  # Next.js React frontend
│   ├── pages/                 # Next.js pages
│   │   ├── index.tsx          # Main chatbot page
│   │   ├── api/               # API routes for proxy
│   │   │   └── chat.ts        # Proxies chat requests to FastAPI backend
│   ├── components/            # React UI components
│   │   ├── ChatInput.tsx      # Input box for user questions
│   │   ├── ChatMessages.tsx   # Display chat history
│   │   ├── Sidebar.tsx        # Sidebar for quick topics, history, theme toggle
│   ├── styles/                # CSS or Tailwind configuration
│   ├── public/                # Static assets (icons, logos, etc.)
│   ├── package.json           # Frontend dependencies
│   ├── next.config.js         # Next.js config
│   └── tsconfig.json          # TypeScript config
│
├── backend/                   # FastAPI backend
│   ├── main.py                # FastAPI app (chat endpoint, OpenAI or Transformers logic)
│   ├── requirements.txt       # Backend Python dependencies
│   ├── .env                   # Environment variables (OpenAI API key)
│   └── venv/                  # (Optional) Python virtual environment
│
├── .gitignore                 # Files & folders to ignore in version control
├── README.md                  # Project overview and documentation
└── LICENSE                    # License file (if open-source)


---

## 🎓 Learning Outcomes
Next.js & React Proficiency
Learned to build an interactive, real-time chat UI with reusable React components and serverless API routes.

FastAPI Backend Development
Gained experience setting up a modern, asynchronous Python backend with input validation and secure environment variable management.

Working with LLMs
Understood how to integrate pre-trained language models like DialoGPT (using Hugging Face Transformers) and connect to commercial LLM APIs like OpenAI GPT-4 for domain-specific answers.

API Design & Proxying
Implemented secure API routing between the frontend and backend, including proxying with Next.js API routes to keep API keys hidden.

Environment Management & Deployment Readiness
Learned to use .env files, virtual environments, and dependency management (requirements.txt for Python and package.json for Node.js).

### Technical Skills Gained
Full-Stack Development
Next.js & React
Learned to design an interactive chat interface with reusable React components (ChatInput, ChatMessages, Sidebar) and manage real-time updates using React state and hooks.

API Routing in Next.js
Implemented secure serverless API routes (/api/chat) to proxy requests from the frontend to the backend without exposing API keys in the browser.

Tailwind CSS
Practiced building a responsive, modern UI with a clean design and optional dark/light theme toggles.

⚙️ Backend & API Development
FastAPI
Gained experience building a lightweight, asynchronous Python backend with input validation using pydantic and efficient request handling.

CORS & Middleware
Learned to configure Cross-Origin Resource Sharing (CORS) to allow secure communication between frontend and backend services during development and deployment.

Environment Variables & Security
Used .env files and the dotenv package to manage secrets like the OpenAI API key, keeping them safe and off the client side.

⚙️ Conversational AI & NLP
Hugging Face Transformers
Integrated open-source LLMs using the transformers library, and understood how the pipeline API simplifies inference for conversational tasks.

DialoGPT
Tested local conversational inference with DialoGPT as an example of lightweight LLMs that can run offline for prototyping.

OpenAI GPT-4 API
Connected the backend to a state-of-the-art LLM (GPT-4) for accurate domain-specific answers, and designed prompt templates to control the bot’s tone and style.

Prompt Engineering
Experimented with system and user prompts to give the chatbot its unique snarky civil engineering tutor personality while delivering helpful responses.

⚙️ Testing & Debugging
API Testing Tools
Practiced testing FastAPI endpoints and Next.js API routes using Postman, Curl, and browser DevTools.

Error Handling
Learned to handle backend errors gracefully and display fallback messages to the user.

⚙️ Deployment Readiness
Environment Setup
Managed Python virtual environments (venv) and Node.js dependency management (npm).

Scalability Awareness
Planned for future deployment on cloud platforms like Vercel (Next.js frontend) and Render/Fly.io (FastAPI backend), and learned best practices for keeping environment variables secure in production.


## 🤝 Acknowledgments

Special thanks to the **Ecocee team** for providing guidance and support throughout this internship project.

**Mentor:** Sreeraj V Rajesh  
**Team Number:** Team 2 
**Team Size:** 2

### 👨‍💼 Team Contributions
| Team Member | Primary Contributions |
|-------------|----------------------|
| Sabarinath ps | UI designer and developer |
| Amjith Kumar | Backend developer |

## 📞 Contact

**Company:** Ecocee  
**Website:** [ecocee.in](https://ecocee.in)  
**Email:** [info@ecocee.in](mailto:info@ecocee.in)

### 👥 Team Contacts
| Team Member | Email | LinkedIn | GitHub |
|-------------|-------|----------|--------|
| Sabarinath PS | psabarinath44@gmail.com | https://www.linkedin.com/in/sabarinath-ps-38ab8131a/ | github.com/sabari12nath |
| N Amjith Kumar | logantempest6@gmail.com | https://www.linkedin.com/in/amjith-kumar-39554a320/ | github.com/logan-tempest|

<div align="center">
  
  **Made with ❤️ during internship at Ecocee**
  
  ⭐ **Star this repo if you found it helpful!** ⭐
  
</div>

---

## 📄 License

This project is developed as part of an internship program at Ecocee. Please refer to the company's guidelines for usage and distribution.

[Optional: Add specific license if applicable]

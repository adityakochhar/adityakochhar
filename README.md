# Hi, I'm Aditya Kochhar 👋

**Full-stack Computer Science undergraduate** at Chitkara University, Punjab (B.Tech CSE, 2023–2027).

I build end-to-end products with **Node.js/Express, MongoDB and React**, with **Java/Spring Boot** for backend breadth. Recently, I've started building with **LLMs and AI agents**. Most of what I know, I learned by building the projects below — breaking them, reading the docs, and fixing them.

- 🔭 Currently building: **AI agents with safety guardrails**, and backend systems focused on auth, caching, and real-time events
- 🌱 Currently learning: **RAG, vector search, and LLM evaluation**
- 💬 Ask me about: AI agent guardrails, JWT auth flows, Redis caching, WebSocket lifecycles, schema design
- 📫 Reach me: **adityakochhar2005@gmail.com**

---

## 🛠 Tech Stack

**Backend**
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat&logo=socketdotio&logoColor=white)

**AI & ML**
![LLM APIs](https://img.shields.io/badge/LLM_APIs-412991?style=flat&logo=openai&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)

**Languages**
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)

**Databases & Caching**
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)

**Frontend**
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)

**Tools & Cloud**
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat&logo=postman&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

**CS Fundamentals** — Data Structures & Algorithms · DBMS · Operating Systems · Computer Networks · OOP · System Design

---

## 📌 Projects

### 🛒 AI Shopping Agent with Spending Limits
`Python` · `FastAPI` · `LLM API` · `scikit-learn` · `Razorpay (test mode)`

An AI that shops online for a user but can never spend more than the user allows. Built for the Razorpay AI Buildathon 2026.

- **Spending rules:** the user sets a limit, allowed categories, allowed shops, and an expiry time — digitally signed (Ed25519), so nobody can change them
- **Permission check:** the AI can't pay by itself; a separate rule-based gate checks every purchase and returns ALLOW, DENY, or ESCALATE
- **Category check:** a small ML classifier checks what the product really is, so a seller can't lie about it — and asks the user when unsure
- **Result:** in 30 test runs, the AI made zero purchases outside the rules; works with the Groq API or a local Ollama model

[Source Code](https://github.com/adityakochhar/ai-shopping-agent)

---

### 📚 Learn Sphere — Learning Management System
`Node.js` · `Express` · `MongoDB` · `Redis` · `WebSockets` · `React.js`

An online learning platform where students take courses, admins manage content, and everyone gets live notifications.

- JWT-based authentication with role-based access control, using reusable middleware for auth, permission checks, and request validation
- Redis caching on frequently requested course and profile routes to cut repeated database reads
- WebSocket-based real-time notifications with connect/disconnect lifecycle handling

[Source Code](https://github.com/adityakochhar/LearnSphere) · [Live Demo](https://learn-sphere-silk-iota.vercel.app/)

---

### 🗂 SyncBoard — Real-Time Collaborative Kanban Board
`React.js` · `Node.js` · `Socket.io`

A multi-user Kanban board where every task movement syncs live across clients, with no page refresh.

- Socket-based user presence tracking across active sessions
- Optimistic UI updates in React that reconcile on server confirmation, keeping state consistent under concurrent edits

[Source Code](https://github.com/adityakochhar/SyncBoard) · [Live Demo](https://sync-board-psi.vercel.app/)

---

### 💳 Payment Gateway Simulator
`Spring Boot` · `MySQL` · `Redis`

A payment backend that works like UPI: it creates payments, moves them through each step, and makes sure no one is charged twice.

- Idempotent transaction APIs backed by a strict state machine: `INITIATED → PROCESSING → SUCCESS/FAILED`
- Exponential-backoff retry logic and Redis-based deduplication to prevent duplicate charges
- Optimistic locking for concurrent updates, plus webhook callbacks for downstream state notifications

[Source Code](https://github.com/adityakochhar/Payment-Gateway-Simulator-) · [Live Demo](https://calm-klepon-3255f0.netlify.app/)

---

### 🎓 EduEnroll — Student Course Enrollment System
`Spring Boot` · `MySQL` · `Spring Security`

A course registration system where students sign up for courses and admins manage them.

- 16-endpoint idempotent REST API supporting student and admin flows
- Normalized MySQL schema across 5 tables with JPA entity mappings and query-level indexing
- Role-based authorization via Spring Security; JUnit integration tests covering auth flows and edge cases

[Source Code](https://github.com/adityakochhar/EduEnroll) · [Live Demo](https://edu-enroll-seven.vercel.app/)

---

### 🌾 Agrisense — IoT Smart Irrigation System
`Arduino` · `Embedded C` · `NPK & Soil Moisture Sensors`

An independent hardware project: a smart soil monitoring and irrigation system that reads live soil data and drives irrigation decisions from it. **4th position at DICE TECHNOVATE 2024.**

---

## 🏆 Achievements

- 🥉 **4th Position — DICE TECHNOVATE 2024** for Agrisense (IoT smart irrigation system)
- ✅ **HackerRank Certified — Java (Basic)**
- ☁️ **AWS AI/ML Workshop, IIT Roorkee**; completed **AWS Cloud Club ML Camper** and **DSA Workshop by Coding Blocks**
- 📊 **CGPA 9.10** (latest SGPA 9.81)

---



## 🤝 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/aditya-kochhar-b7060b295/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:adityakochhar2005@gmail.com)

*Open to internship and full-time opportunities in full-stack, backend, AI, and software engineering roles.*

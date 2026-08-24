# Hi, I'm Aditya Kochhar 👋

**Backend-focused Computer Science undergraduate** at Chitkara University, Punjab (B.Tech CSE, 2023–2027).

I build REST APIs and real-time systems with **Java/Spring Boot** and **Node.js/Express**, and I'm steadily growing into genuine full-stack work with **React.js**. Most of what I know, I learned by building the projects below — breaking them, reading the docs, and fixing them.

- 🔭 Currently building: backend systems with a focus on **auth, caching, and real-time events**
- 🌱 Currently learning: **React internals** (re-render behaviour, `memo`, `useCallback`, `useMemo`) and **AI/LLM fundamentals**
- 💬 Ask me about: JWT auth flows, Redis caching, WebSocket lifecycles, schema design
- 📫 Reach me: **adityakochhar2005@gmail.com**

---

## 🛠 Tech Stack

**Backend**
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=springboot&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat&logo=express&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat&logo=jsonwebtokens&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat&logo=socketdotio&logoColor=white)

**Languages**
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=cplusplus&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=mysql&logoColor=white)

**Databases & Caching**
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
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

### 💳 Payment Gateway Simulator
`Spring Boot` · `MySQL` · `Redis`

A UPI-inspired payment processing backend built to understand how real transaction systems stay correct under failure.

- Idempotent transaction APIs backed by a strict state machine: `INITIATED → PROCESSING → SUCCESS/FAILED`
- Exponential-backoff retry logic and Redis-based deduplication to prevent duplicate charges
- Optimistic locking for concurrent updates, plus webhook callbacks for downstream state notifications

[Repository](https://github.com/adityakochhar/payment-gateway-simulator) · [Live](#)

---

### 📚 Learn Sphere — Learning Management System
`Node.js` · `Express` · `MongoDB` · `Redis` · `WebSockets` · `React.js`

An LMS backend I used to learn Node.js and Express properly, from basic routing up to caching and real-time events.

- JWT-based authentication with role-based access control, using reusable middleware for auth, permission checks, and request validation
- Redis caching on frequently requested course and profile routes to cut repeated database reads
- WebSocket-based real-time notifications with connect/disconnect lifecycle handling

[Repository](https://github.com/adityakochhar/learn-sphere) · [Live](#)

---

### 🎓 EduEnroll — Student Course Enrollment System
`Spring Boot` · `MySQL` · `Spring Security`

A multi-role course registration API focused on clean schema design and defensible endpoint behaviour.

- 16-endpoint idempotent REST API supporting student and admin flows
- Normalized MySQL schema across 5 tables with JPA entity mappings and query-level indexing
- Role-based authorization via Spring Security; JUnit integration tests covering auth flows and edge cases

[Repository](https://github.com/adityakochhar/eduenroll) · [Live](#)

---

### 🗂 SyncBoard — Real-Time Collaborative Kanban Board
`React.js` · `Node.js` · `Socket.io`

A multi-user Kanban board where every task movement syncs live across clients, with no page refresh.

- Socket-based user presence tracking across active sessions
- Optimistic UI updates in React that reconcile on server confirmation, keeping state consistent under concurrent edits

[Repository](https://github.com/adityakochhar/syncboard) · [Live](#)

---

### 🌾 Agrisense — IoT Smart Irrigation System
`Arduino` · `Embedded C` · `NPK & Soil Moisture Sensors`

An independent hardware project: a smart soil monitoring and irrigation system that reads live soil data and drives irrigation decisions from it. **4th position at DICE TECHNOVATE 2024.**

[Repository](https://github.com/adityakochhar/agrisense)

---

## 🏆 Achievements

- 🥉 **4th Position — DICE TECHNOVATE 2024** for Agrisense (IoT smart irrigation system)
- ✅ **HackerRank Certified — Java (Basic)**
- 🎯 **Top performer — Flipkart GRiD 6.0 Level 1 Tech Quiz**, Software Development Track
- ☁️ **AWS AI/ML Workshop, IIT Roorkee**; completed **AWS Cloud Club ML Camper** and **DSA Workshop by Coding Blocks**
- 📊 **CGPA 9.10** (latest SGPA 9.81)

---

## 📈 GitHub Activity

<!-- These render automatically once your username is correct. Delete this section if you'd rather not show stats. -->
![Aditya's GitHub stats](https://github-readme-stats.vercel.app/api?username=adityakochhar&show_icons=true&hide_border=true)
![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=adityakochhar&layout=compact&hide_border=true)

---

## 🤝 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR-LINKEDIN-HANDLE)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:adityakochhar2005@gmail.com)

*Open to internship and full-time opportunities in backend, full-stack, and software engineering roles.*

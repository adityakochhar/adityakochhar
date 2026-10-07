<div align="center">

# Hi, I'm Aditya Kochhar 👋

**Backend-leaning full-stack developer · B.Tech CSE at Chitkara University, Punjab (Class of 2027)**

I like building the parts of software that have to be right every time:<br>
two people clicking the same seat, a payment sent twice, an AI agent trying to overspend.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=data:image/svg%2Bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTIwLjQ0NyAyMC40NTJoLTMuNTU0di01LjU2OWMwLTEuMzI4LS4wMjctMy4wMzctMS44NTItMy4wMzctMS44NTMgMC0yLjEzNiAxLjQ0NS0yLjEzNiAyLjkzOXY1LjY2N0g5LjM1MVY5aDMuNDE0djEuNTYxaC4wNDZjLjQ3Ny0uOSAxLjYzNy0xLjg1IDMuMzctMS44NSAzLjYwMSAwIDQuMjY3IDIuMzcgNC4yNjcgNS40NTV2Ni4yODZ6TTUuMzM3IDcuNDMzYy0xLjE0NCAwLTIuMDYzLS45MjYtMi4wNjMtMi4wNjUgMC0xLjEzOC45Mi0yLjA2MyAyLjA2My0yLjA2MyAxLjE0IDAgMi4wNjQuOTI1IDIuMDY0IDIuMDYzIDAgMS4xMzktLjkyNSAyLjA2NS0yLjA2NCAyLjA2NXptMS43ODIgMTMuMDE5SDMuNTU1VjloMy41NjR2MTEuNDUyek0yMi4yMjUgMEgxLjc3MUMuNzkyIDAgMCAuNzc0IDAgMS43Mjl2MjAuNTQyQzAgMjMuMjI3Ljc5MiAyNCAxLjc3MSAyNGgyMC40NTFDMjMuMiAyNCAyNCAyMy4yMjcgMjQgMjIuMjcxVjEuNzI5QzI0IC43NzQgMjMuMiAwIDIyLjIyMiAwaC4wMDN6Ii8%2BPC9zdmc%2B)](https://www.linkedin.com/in/aditya-kochhar-b7060b295/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:adityakochhar2005@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/7527913755/)

</div>

## 👨‍💻 About me

Most of what I know, I learned by building the projects below: breaking them, reading the docs, and fixing them.

- 🛠 I mostly build backends in **Node.js/Express** and **Java/Spring Boot**, with **React + TypeScript** on the front end
- 🤖 Lately building **AI agents with safety guardrails** in Python
- 🌱 Learning **RAG, vector search and LLM evaluation**
- 💬 Ask me about race conditions, idempotent APIs, JWT auth, Redis caching and Socket.IO
- 🎯 Open to **internships and full-time roles** in backend, full-stack and software engineering

## 🎟️ Featured: SeatWise

**A cinema seat-booking app where seats update live for everyone viewing the same show.**

`TypeScript` `React` `Node.js` `Express` `MongoDB` `Socket.IO` `TanStack Query` `Tailwind CSS` `Jest` `Docker`

<a href="https://github.com/adityakochhar/SeatWise"><img src="https://raw.githubusercontent.com/adityakochhar/SeatWise/main/screenshots/seats.png" alt="SeatWise seat selection screen" width="100%"></a>

- **Two people, one seat, one winner.** Each seat is claimed with a single conditional MongoDB update, so when two people click the same seat at the same moment, only one gets it. If a request loses any of its seats, it gives back the ones it did get. A test sends two requests for the same seat at once and checks that exactly one wins.
- **5-minute holds.** Held seats show a countdown at checkout and go back on sale when time runs out. The expiry is a stored timestamp, so an expired hold counts as free even after a server restart, and a background job clears old holds every 30 seconds.
- **Live seat map.** Socket.IO rooms push every hold, booking, release and expiry to everyone viewing that show.
- **Also:** JWT login, an admin dashboard (cinemas, screens, movies, shows, revenue and occupancy), simulated payment, ticket emails through Brevo, 19 API tests, GitHub Actions CI and Docker Compose.

[**Source code**](https://github.com/adityakochhar/SeatWise) · [**Live demo**](https://seatwise-0njd.onrender.com)

<sub>The demos run on free hosting, so the first load can take about a minute. SeatWise's demo logins are in its README.</sub>

## 📂 More projects

### 🛒 AI Shopping Agent with Spending Limits (Mandate)

**An AI agent that shops for you but can only spend inside limits you sign.** Built for the Razorpay AI Buildathon 2026.

`Python` `FastAPI` `scikit-learn` `Ed25519 (PyNaCl)` `Groq / Ollama` `Razorpay (test mode)`

- The LLM only *suggests* a purchase. A separate rule-based gate checks it against a signed spending mandate (limit, categories, shops, expiry) and answers ALLOW, DENY or ESCALATE. Payment code is only reachable on ALLOW.
- A small scikit-learn classifier (73% accuracy on held-out data) works out what the product really is, so a seller can't label batteries as "groceries" to get past the rules. When the classifier isn't confident, the purchase goes to the user instead.
- In a 30-scenario batch run: **0 purchases outside the rules** and 0 valid purchases blocked. I wrote these scenarios myself, so this isn't adversarial testing yet.

[**Source code**](https://github.com/adityakochhar/ai-shopping-agent)

### 💳 Payment Gateway Simulator

**A UPI-style payment backend that won't charge twice for the same request.**

`Java 17` `Spring Boot 3` `MySQL` `Redis` `JUnit 5` `React` `Docker`

- Payments follow a strict state machine, `INITIATED → PROCESSING → SUCCESS / FAILED`, with no skipping and no going back.
- **Idempotency:** retrying with the same key returns the same payment. A `UNIQUE` column in MySQL guarantees it, Redis caches keys for 24 hours (falling back to MySQL if Redis is down), and reusing a key with a different amount returns `409 Conflict`.
- Stuck payments retry with exponential backoff (2 s, 4 s, 8 s), JPA optimistic locking (`@Version`) stops two updates from overwriting each other, and every final state logs a simulated webhook.

[**Source code**](https://github.com/adityakochhar/Payment-Gateway-Simulator-) · [**Live demo**](https://calm-klepon-3255f0.netlify.app/)

### 📚 Learn Sphere

**One place for scattered college study material.** Students browse it by branch, year and subject; admins upload and organise it.

`Node.js` `Express` `MongoDB` `Redis` `Socket.IO` `React` `Jest`

- JWT login with an admin role, plus a Redis-based login lockout: 3 failed attempts lock the account for 30 minutes.
- Redis caching on the subject and content routes (skipped automatically when Redis is down), and Socket.IO notifications when new material is added to a subject.
- 100+ Jest and Supertest tests for the server.

[**Source code**](https://github.com/adityakochhar/LearnSphere) · [**Live demo**](https://learn-sphere-silk-iota.vercel.app/)

### 🎓 EduEnroll

**Course enrollment split into two Spring Boot services, each with its own MySQL database.**

`Java` `Spring Boot` `Spring Security` `MySQL` `React` `Docker`

- `student-service` handles sign-up, login (JWT + BCrypt) and enrollments, with USER and ADMIN roles in Spring Security.
- `course-service` manages courses and talks to the student service over REST; deleting a course also removes it from every student's enrollments.
- 16 REST endpoints across the two services, a React front end and a Dockerfile for each service.

[**Source code**](https://github.com/adityakochhar/EduEnroll) · [**Live demo**](https://edu-enroll-seven.vercel.app/)

### 🧩 Smaller builds

| Project | What it is |
|:--|:--|
| [**SyncBoard**](https://github.com/adityakochhar/SyncBoard) | A shared Kanban board: card moves sync live between browsers over Socket.IO, with presence (who's online, who's dragging which card). The board lives in server memory and the latest update wins. [Live demo](https://sync-board-psi.vercel.app/) |
| **Agrisense** | An Arduino soil-monitoring and irrigation system using NPK and soil-moisture sensors. 4th place at DICE TECHNOVATE 2024. (Hardware project, no code repo.) |

## 🧰 Tech stack

| Area | Tools |
|:--|:--|
| **Languages** | ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **Backend** | ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=flat-square&logo=socketdotio&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white) |
| **Databases** | ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white) |
| **AI / ML** | ![Groq API](https://img.shields.io/badge/Groq_API-F55036?style=flat-square) ![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white) |
| **Testing & DevOps** | ![Jest](https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white) ![JUnit 5](https://img.shields.io/badge/JUnit_5-25A162?style=flat-square&logo=junit5&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) |

**CS fundamentals:** Data Structures & Algorithms · DBMS · Operating Systems · Computer Networks · OOP · System Design

## 🏆 Achievements

- 🏅 **4th place, DICE TECHNOVATE 2024** for Agrisense
- 💻 **200+ LeetCode problems** solved, mostly in Java
- ✅ **HackerRank certified:** Java (Basic)
- ☁️ **AWS AI/ML Workshop** at IIT Roorkee · **AWS Cloud Club ML Camper** · **DSA Workshop** by Coding Blocks
- 📊 **CGPA 9.10** (latest SGPA 9.81)

<div align="center">
<sub>Thanks for stopping by. The quickest way to reach me is <a href="mailto:adityakochhar2005@gmail.com">email</a>.</sub>
</div>

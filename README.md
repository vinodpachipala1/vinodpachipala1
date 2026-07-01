<h1 align="center">Vinod Pachipala</h1>

<p align="center">
Full Stack Developer • PERN Stack Developer
</p>

<p align="center">
  <a href="mailto:vinodpachipala93@gmail.com">Email</a> •
  <a href="https://github.com/vinodpachipala1">GitHub</a> •
  <a href="https://www.linkedin.com/in/vinod-pachipala-891375372/">LinkedIn</a> •
  <a href="https://portfolio-chi-pink-42.vercel.app">Portfolio</a>
</p>

---

## About Me

I am an Integrated M.Tech Computer Science student at VIT Amaravati (Expected May 2027) with strong hands-on experience building full-stack web applications using the PERN stack.

I've solved 300+ Data Structures and Algorithms problems, and I'm interested in scalable backend systems, relational database design, real-time communication workflows, authentication systems, and AI-integrated applications.

I enjoy building systems that solve real workflow problems — role-based platforms, transactional data integrity, real-time sync — rather than static demo projects.

---

## Education

| Institution | Detail | Score | Duration |
|---|---|---|---|
| Vellore Institute of Technology, Amaravati | Integrated M.Tech in Computer Science and Engineering | CGPA: 8.28 / 10 | Nov 2022 – May 2027 (Expected) |
| KSN Junior College | Board of Intermediate Education, Andhra Pradesh | 881/1000 (88.1%) | Aug 2020 – Jun 2022 |
| Pratibha Vidyaniketan EM School, Samalkot | Board of Secondary Education, Andhra Pradesh | 570/600 (95%) | Mar 2020 |

---

## Tech Stack

| Category | Technologies |
|---|---|
| Languages | ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?logo=javascript&logoColor=black&style=flat) ![Java](https://img.shields.io/badge/-Java-007396?logo=java&logoColor=white&style=flat) ![SQL](https://img.shields.io/badge/-SQL-336791?style=flat) |
| Frontend | ![React](https://img.shields.io/badge/-React-61DAFB?logo=react&logoColor=black&style=flat) ![React Router](https://img.shields.io/badge/-React%20Router-CA4245?logo=reactrouter&logoColor=white&style=flat) ![TailwindCSS](https://img.shields.io/badge/-TailwindCSS-38B2AC?logo=tailwind-css&logoColor=white&style=flat) ![Axios](https://img.shields.io/badge/-Axios-5A29E4?logo=axios&logoColor=white&style=flat) ![Framer Motion](https://img.shields.io/badge/-Framer%20Motion-0055FF?logo=framer&logoColor=white&style=flat) ![HTML5](https://img.shields.io/badge/-HTML5-E34F26?logo=html5&logoColor=white&style=flat) ![CSS3](https://img.shields.io/badge/-CSS3-1572B6?logo=css3&logoColor=white&style=flat) |
| Backend | ![Node.js](https://img.shields.io/badge/-Node.js-339933?logo=node.js&logoColor=white&style=flat) ![Express.js](https://img.shields.io/badge/-Express.js-000000?logo=express&logoColor=white&style=flat) ![Socket.IO](https://img.shields.io/badge/-Socket.IO-010101?logo=socket.io&logoColor=white&style=flat) ![JWT](https://img.shields.io/badge/-JWT-black?logo=JSON%20web%20tokens&style=flat) ![bcrypt](https://img.shields.io/badge/-bcrypt-8B4513?style=flat) ![Multer](https://img.shields.io/badge/-Multer-FF6600?style=flat) ![Brevo API](https://img.shields.io/badge/-Brevo%20API-0B996E?style=flat) ![Nodemailer](https://img.shields.io/badge/-Nodemailer-22B573?style=flat) |
| AI / APIs | ![Gemini API](https://img.shields.io/badge/-Gemini%20API-8E75B2?logo=googlegemini&logoColor=white&style=flat) |
| Databases | ![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-336791?logo=postgresql&logoColor=white&style=flat) ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?logo=mysql&logoColor=white&style=flat) |
| Core CS | Data Structures & Algorithms, OOP, Operating Systems, DBMS |
| Tools | ![Git](https://img.shields.io/badge/-Git-F05032?logo=git&logoColor=white&style=flat) ![GitHub](https://img.shields.io/badge/-GitHub-181717?logo=github&logoColor=white&style=flat) ![Postman](https://img.shields.io/badge/-Postman-FF6C37?logo=postman&logoColor=white&style=flat) |
| Deployment | ![Vercel](https://img.shields.io/badge/-Vercel-000000?logo=vercel&logoColor=white&style=flat) ![Render](https://img.shields.io/badge/-Render-46E3B7?logo=render&logoColor=black&style=flat) |
| AI Tools | ChatGPT, Gemini, Claude |

---

# Featured Projects

## PrimeCart — Full Stack E-Commerce Platform

🔗 [Repository](https://github.com/vinodpachipala1/ecommerce) • [Live Demo](https://ecommerce-theta-rose-83.vercel.app)

**Tech:** React.js, React Router DOM, Socket.IO Client, Axios, Tailwind CSS · Node.js, Express.js, PostgreSQL, JWT, bcryptjs, Multer

### Architecture
Layered backend: **Routes → Controllers → Services → Modules → PostgreSQL**, separating request handling, business logic, and raw SQL queries into distinct layers for maintainability.

### Key Features
- 17 REST API endpoints across auth, product, seller-product, cart, and order flows
- Dual-role system (customer/seller) with JWT authentication and an `optionalAuth` middleware that allows both guest and logged-in product browsing
- Real-time events via Socket.IO — `productAdded`, `productDeleted`, `stockUpdated`, `newOrder`, and live order-status updates pushed to both customer and seller dashboards
- Multer-based product image upload for seller inventory management
- Full cart → checkout → order-tracking workflow with address handling

### Engineering Highlights
- Order placement runs as a single atomic transaction — validates stock, creates the grouped order, decrements inventory, and clears the cart in one commit, preventing partial writes under concurrent submissions
- bcrypt password hashing and JWT-based route protection across 17 endpoints
- Real-time inventory synchronization designed to keep customer and seller views consistent without polling

---

## Job Board System

🔗 [Repository](https://github.com/vinodpachipala1/JobBoard) • [Live Demo](https://job-board-seven-ashen.vercel.app)

**Tech:** React.js, React Router, Tailwind CSS, Axios · Node.js, Express.js, JWT, bcryptjs, Multer, Brevo Email API

### Key Features
- ~21 REST API endpoints spanning auth, candidate profiles, company management, job postings, and applications
- OTP-based registration verification via the Brevo transactional email API — 6-digit OTP, 5-minute expiry, auto-deleted after successful activation
- Secure PDF resume upload and protected retrieval using Multer, with unique file naming
- Full candidate ↔ employer application lifecycle: apply → track → status update, with automated email notifications (application confirmation, hiring-stage changes) sent via Brevo
- Employer analytics view — total jobs posted, total applications, hiring statistics

### Engineering Highlights
- Eliminated duplicate applications by replacing an application-layer check with a DB-level UNIQUE constraint on `(candidate_id, job_id)`, closing the race-condition window permanently
- Normalized relational schema separating users, companies, jobs, applications, candidate profiles, and OTP records
- Modular backend structure (routes/controllers/models/middleware) with role-separated candidate and employer workflows

---

## QuizMaster — Online Quiz Platform

🔗 [Repository](https://github.com/vinodpachipala1/QuizMaster) • [Live Demo](https://quiz-master-ivory.vercel.app)

**Tech:** React.js, React Router DOM, Axios, Tailwind CSS, Framer Motion · Node.js, Express.js, PostgreSQL (pg), bcryptjs, JWT

### Key Features
- 10 REST API endpoints across auth, quiz management, and attempt tracking
- 3-table PostgreSQL schema (`users`, `quizzes`, `attempts`) storing questions as JSONB — avoids a separate per-question join table while supporting variable-length question arrays
- Timed quiz-attempt workflow with auto-submission on timer expiry and live score calculation
- Per-user analytics dashboard: created quizzes, attempt history, best-score tracking, and attempt counts, persisted server-side across sessions
- Deployed frontend (Vercel) and backend (Render) with environment-restricted CORS

### Engineering Highlights
- Hardened all 10 REST API endpoints against SQL injection using parameterized PostgreSQL queries (`WHERE id = $1`)
- JSONB-based question storage traded per-question query granularity for simpler schema design and faster iteration — a deliberate schema tradeoff
- Layered backend architecture (routes → controllers → models) for maintainability and easier debugging

---

## Postathon — India Post Hackathon Project

🔗 [Repository](https://github.com/vinodpachipala1/hackathon-Postathon) • [Live Demo](https://hackathon-postathon.vercel.app)

**Tech:** React.js, React Router, Tailwind CSS, Axios · Node.js, Express.js, PostgreSQL, JWT, Nodemailer, Gemini AI (`@google/genai`)

### Key Features
- Two independently-scoped OTP systems: registration OTP (creates the complaint) and tracking OTP (secure read-only complaint lookup), preventing security overlap between the two flows
- AI-powered complaint analysis pipeline via Gemini — generates category, department assignment, sentiment score, priority level (LOW–CRITICAL), and an auto-drafted acknowledgement response
- Officer dashboard with live complaint statistics, status/priority filters, keyword search, and dynamic "urgent attention" flagging (complaints unresolved after 48 hours)
- Multi-language translation system (Gemini 2.5 Flash) with response caching, a 10-second timeout, and a LibreTranslate fallback if the primary AI call fails
- Automated email notifications at every stage — OTP delivery, complaint acknowledgement, investigation-started, and resolution

### Engineering Highlights
- Designed an AI fail-safe: if the Gemini call fails, the complaint still gets created with a default priority and response instead of blocking the workflow — production-style graceful degradation
- Dynamic urgency detection computed from complaint age and status rather than a static flag
- Complaint IDs generated in a structured `IP-CMP-XXXXXX` format for traceability across officer and citizen views

---

## Real-Time Budget Splitter

🔗 [Repository](https://github.com/vinodpachipala1/Expense-Splitter) • [Live Demo](https://expense-splitter-xi-two.vercel.app)

**Tech:** React.js, Node.js, Express.js, PostgreSQL

### Key Features
- Group expense management system
- Shared balance tracking
- Settlement and archive workflows
- Multi-user collaborative expense management

### Engineering Highlights
- Implemented session-based authentication architecture
- Designed relational workflows for shared financial calculations
- Solved deployment and cross-origin session persistence issues

---

## Achievements

### Google Big Code 2026 — Top 1,500 Nationally (HackerEarth)
- Advanced to Round 2 of Google India's Big Code championship among the top 1,500 engineering students nationwide after clearing aptitude and multi-round DSA elimination rounds

### Postathon — India Post Hackathon — 2nd Place / 150 Teams
- Secured 2nd place among 150 teams in a 24-hour hackathon by building a grievance management system for India Post
- Built an AI-assisted grievance platform with OTP-based verification, Gemini-driven complaint classification and sentiment analysis, and officer-side tracking workflows

---

## Certifications

- Complete Web Development Bootcamp — Udemy (2024)
- Deloitte Australia — Technology Job Simulation — Forage (2026)

---

## GitHub Statistics

<p align="center">
  <img src="https://github-readme-stats.anuraghazra1.vercel.app/api?username=vinodpachipala1&show_icons=true&theme=react" width="49%"/>
  <img src="https://github-readme-stats.anuraghazra1.vercel.app/api/top-langs/?username=vinodpachipala1&layout=compact&theme=react" width="49%"/>
</p>

## Contact

- Email: vinodpachipala93@gmail.com
- LinkedIn: https://www.linkedin.com/in/vinod-pachipala-891375372/
- GitHub: https://github.com/vinodpachipala1
- Portfolio: https://portfolio-chi-pink-42.vercel.app
- TakeUForward: [Profile](https://takeuforward.org/)

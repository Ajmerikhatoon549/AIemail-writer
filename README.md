# 📧 AI Email Reply Generator

An AI-powered web application that generates smart email replies using the **Gemini API**. The frontend is built with React + Vite and served directly from the Spring Boot backend's static folder, containerized with Docker, and deployed on Render.

🔗 **Live Demo** → [aiemail-writer-xkkz.onrender.com](https://aiemail-writer-xkkz.onrender.com/)

🔌 **Chrome Extension Repo** (runs locally, integrated into Gmail) → [email-reply-extension](https://github.com/Ajmerikhatoon549/email-reply-extension)

---

## 🚀 Features

- ✉️ Paste any email and get an intelligent reply instantly
- 🎨 Choose reply tone — Professional, Friendly, Formal, Casual, and more
- ⚡ React + Vite frontend served via Spring Boot static folder
- 🔒 Spring Boot backend powered by Gemini API
- 🐳 Dockerized for deployment (Render has no native Java environment)
- ☁️ Live on Render via Docker container

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React, Vite |
| Backend | Spring Boot (Java) |
| AI Model | Google Gemini API |
| Containerization | Docker |
| Deployment | Render (via Dockerfile) |

---

## 📁 Project Structure

```
email-reply-generator/
├── src/
│   └── main/
│       ├── java/               # Spring Boot backend source
│       └── resources/
│           └── static/         # React build output (frontend)
├── frontend/                   # React + Vite source
│   ├── src/
│   │   ├── components/
│   │   └── App.jsx
│   └── package.json
├── Dockerfile
└── pom.xml
```

---

## ⚙️ Getting Started

### Prerequisites

- Java 21
- Node.js 18+
- Docker
- Google Gemini API Key → [Get it here](https://aistudio.google.com/)

---

### 🔧 Local Setup

**1. Build the React frontend:**

```bash
cd frontend
npm install
npm run build
```

> Build output goes into `src/main/resources/static/`

**2. Run the Spring Boot backend:**

```bash
./mvnw spring-boot:run
```

App runs at `http://localhost:8080`

---

### 🐳 Docker Setup

```bash
docker build -t email-reply-generator .
docker run -p 8080:8080 -e GEMINI_API_KEY=your_key_here email-reply-generator
```

---

## 🌍 Deployment on Render

Render does not provide a native Java environment, so the app is containerized with Docker and deployed as a Docker-based web service.

**Steps:**
1. Push your code to GitHub
2. Go to [Render](https://render.com) → New → **Web Service**
3. Connect your GitHub repo
4. Select **Docker** as the environment
5. Add environment variable: `GEMINI_API_KEY` in Render dashboard
6. Deploy!

---

## 🔌 Chrome Extension

The Chrome Extension is **not deployed** — it runs locally and is integrated directly into my own Gmail.

Source code available here → [email-reply-extension](https://github.com/Ajmerikhatoon549/email-reply-extension)

---

## 📸 Screenshots

> assets/homepage.png
> assets/GeneratedReply.png
> assets/AIReplyButton-on-Email.png
> assets/ReplyByAI-Reply.png


## 👩‍💻 Author

**Ajmeri Khatoon**
[GitHub](https://github.com/Ajmerikhatoon549)

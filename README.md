# 📝 MERN Blog Platform – DevOps & Deployment Essentials

A **MERN stack** blog platform designed to help users **create**, **edit**, **delete**, and **publish blog posts**. This project emphasizes best practices in **DevOps**, including **CI/CD pipelines**, **monitoring**, and **secure deployment** on cloud platforms.

> Part of **Week 7** of the DevOps and Deployment Essentials module.

---

## 🚀 Project Overview

The MERN Blog Platform allows for:

* ✍️ Creating, editing, and deleting blog posts
* 📚 Viewing blog articles in a public feed
* 🔐 Admin authentication for post management
* 🧪 CI/CD automation with GitHub Actions
* 🌐 Full deployment: **Backend** (Render) + **Frontend** (Vercel)
* 🔍 Logging and monitoring using Winston, Morgan, and Sentry

---

## 🔧 Technologies Used

### 💻 Stack

* **MongoDB** – Database
* **Express.js** – Backend server
* **React.js** – Frontend UI
* **Node.js** – Runtime

### 🧰 DevOps & Tooling

* **GitHub Actions** – CI/CD Pipeline
* **Render** – Backend Deployment
* **Vercel** – Frontend Deployment
* **PM2** – Backend process manager
* **Sentry** – Frontend error tracking
* **Winston & Morgan** – Backend logging

---

## 📦 Project Setup

### 1. Clone the Repository

```bash
git clone https://github.com/rxymitchy/Devops-and-Deployment-essentials.git
cd Devops-and-Deployment-essentials
```

### 2. Backend Setup

```bash
cd mern-blog-platform/backend
npm install
cp .env.example .env
# Add MongoDB URI and JWT_SECRET in .env
npm run dev
```

### 3. Frontend Setup

```bash
cd ../frontend
npm install
npm run dev
```

---

## 🔄 CI/CD with GitHub Actions

* Automatically runs tests on push and pull requests
* Prevents merging with failed builds
* Provides notifications for build status
* `.github/workflows/node.yml` manages the build/test jobs

---

## ☁️ Deployment

### Backend – Render

* Deployed via GitHub integration
* Uses **environment variables** securely managed via Render dashboard
* Process managed with **PM2**

### Frontend – Vercel

* Auto-deployment triggered from `main` branch
* Connects to Render-hosted API via `.env` config
* Optimized with image and bundle compression

---

## 🧪 Testing

* Basic backend route tests with Jest and Supertest
* GitHub Actions runs tests in CI pipeline before merging

---

## 📊 Monitoring & Logging

* **Winston + Morgan** for structured request and error logs
* **Sentry** integrated in React for real-time UI error monitoring
* View logs via Render dashboard

---

## 🔐 Security Practices

* HTTPS enforced on both frontend and backend
* API keys and credentials stored securely in environment variables
* Admin-only routes protected with JWT authentication
* Public routes limited to reading posts

---

## 📁 Folder Structure

```
mern-blog-platform/
├── backend/
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── middleware/
│   ├── tests/
│   └── server.js
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── api/
│   │   └── App.jsx
└── README.md
```

---

## 📈 Future Improvements

* Rich-text editor for writing posts
* Comment system for users
* Role-based access control (Admin vs Reader)
* Enhanced test coverage

---

## 🧑‍💻 Author

Created by [**@rxymitchy**](https://github.com/rxymitchy)
Focused on building production-ready MERN applications with DevOps excellence.

---

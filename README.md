# 🛠️ Project Management Tool

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Tech](https://img.shields.io/badge/tech-stack-FullStack-blueviolet)

A full-stack **Project Management Tool** built with **React (Vite)** on the frontend and **Node.js, Express.js, and SQLite** on the backend. This tool helps users manage projects, assign tasks, and track progress with role-based access and a modern UI.

---

## 🚀 Features

- ✅ User Authentication (Login/Signup)
- 📁 Project Creation & Task Assignment
- 🔐 Role-Based Access Control (Admin/User)
- 📊 Dashboard Overview for Users, Projects, and Tasks
- 🧠 AI-powered User Story Generator (optional)
- 💾 SQLite for local database
- 🎨 Tailwind CSS for UI styling

---

## 🧰 Tech Stack

| Layer      | Technology            |
|------------|------------------------|
| Frontend   | React.js (Vite), Tailwind CSS |
| Backend    | Node.js, Express.js     |
| Database   | SQLite + TypeORM        |
| Deployment | Render, GitHub, Vercel/Netlify |
| Testing    | Postman (for APIs)      |

---

## 📁 Folder Structure

project-management-tool/
│
├── backend/
│ ├── config/ # DB connection
│ ├── controllers/ # Business logic
│ ├── routes/ # API endpoints
│ ├── models/ # DB schemas
│ ├── middleware/ # Auth/error handlers
│ ├── public/ # Frontend build output (after npm run build)
│ ├── server.js # Express entry file
│ ├── .env # Env variables (not pushed)
│
├── frontend/
│ ├── src/
│ │ ├── components/ # Navbar, Cards etc.
│ │ ├── pages/ # Home, Login, Signup, Dashboard
│ │ ├── App.js
│ │ └── main.jsx
│ ├── public/
│ └── vite.config.js
│
├── README.md
└── .gitignore
## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Fairoz-source/Project-model-tool.git
cd Project-model-tool
2. Install Dependencies
Backend
bash
Copy
Edit
cd backend
npm install
Frontend
bash
Copy
Edit
cd ../frontend
npm install
🧪 Running the Project Locally
Start Backend (Port 5000)
bash
Copy
Edit
cd backend
node server.js
API runs at: http://localhost:5000/api

Start Frontend (Port 5173)
bash
Copy
Edit
cd frontend
npm run dev
App runs at: http://localhost:5173

🌐 Deployment Instructions
✅ Deploy Fullstack Together (Render.com)
Build the frontend

bash
Copy
Edit
cd frontend
npm run build
Move the dist/ folder into backend

bash
Copy
Edit
mv dist ../backend/public
Update server.js to serve frontend

js
Copy
Edit
const path = require("path");
app.use(express.static(path.join(__dirname, "public")));
app.get("*", (req, res) => {
  res.sendFile(path.join(__dirname, "public", "index.html"));
});
Push to GitHub, then deploy backend/ on Render

🔐 Environment Variables
Create a .env file inside backend/:

ini
Copy
Edit
PORT=5000
JWT_SECRET=your_super_secret
DB_PATH=./project.db
Add .env to .gitignore to prevent pushing secrets.



Login Page	Dashboard



## ✅ Also Add This `.gitignore` File (Top-level)

```gitignore
# Node.js
node_modules/
.env
.env.*

# SQLite DB
*.sqlite
*.db

# Logs
logs/
*.log

# Frontend Build
frontend/dist
backend/public

# OS & Editor
.DS_Store
*.swp
.vscode/

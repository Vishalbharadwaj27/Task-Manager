# Task Manager

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Node.js](https://img.shields.io/badge/node-%3E%3D14.0.0-green.svg) ![React](https://img.shields.io/badge/react-^18.2.0-blue.svg) ![Next.js](https://img.shields.io/badge/next-14.0.4-black.svg)

---

## 📖 Overview

**Task Manager** is a full‑stack web application that provides a sleek, secure, and responsive platform for managing personal tasks. It features a modern **Next.js** frontend powered by **Tailwind CSS**, and a **Node.js/Express** backend with **MongoDB** for data persistence and **JWT** based authentication.

The UI follows a **premium, glass‑morphic design** with smooth micro‑animations, dark‑mode support, and mobile‑first responsiveness, delivering a polished user experience across devices.

---

## 🛠️ Tech Stack

| Layer | Technologies |
|-------|---------------|
| **Frontend** | Next.js (App Router), React 18, Tailwind CSS, Heroicons |
| **Backend** | Node.js, Express, MongoDB, Mongoose, JWT, Bcrypt.js |
| **Authentication** | JSON Web Tokens (access & refresh), HTTP‑only cookies |
| **DevOps** | npm scripts, nodemon (dev), ESLint, Prettier |
| **Testing** | Jest (future), Cypress (future) |

---

## ✨ Features

- **User Registration & Login** – Secure password hashing with BCrypt and JWT‑based sessions.
- **Profile Management** – Update email, name, and password.
- **Task CRUD** – Create, read, update (toggle completion), and delete tasks.
- **Search & Filters** – Query tasks by keyword, completion status, and due dates.
- **Responsive UI** – Optimised for desktop, tablet, and mobile.
- **Dark‑Mode & Glassmorphism** – Modern aesthetic with subtle shadows and transitions.
- **Health Check Endpoint** – `/api/health` for monitoring.

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** ≥ 14.x
- **npm** (comes with Node) or **yarn**
- **MongoDB** running locally (default port `27017`) or a remote URI.

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/task-manager.git
   cd task-manager/Task-Manager-main
   ```
2. **Backend Setup**
   ```bash
   cd backend
   npm install
   # Create a .env file (see .env.example) with at least:
   # MONGODB_URI=mongodb://localhost:27017/taskmanager
   # JWT_SECRET=your_secret_key
   npm run dev   # Starts server at http://localhost:5000
   ```
3. **Frontend Setup**
   ```bash
   cd ../frontend
   npm install
   # Optionally copy .env.example to .env and set NEXT_PUBLIC_API_URL=http://localhost:5000
   npm run dev   # Starts Next dev server (http://localhost:3000)
   ```

> **Tip**: Keep both terminals open – one for the backend and one for the frontend.

---

## 📚 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/auth/register` | Register a new user |
| `POST` | `/api/auth/login` | Authenticate and receive JWT |
| `GET` | `/api/auth/me` | Retrieve current user profile |
| `GET` | `/api/user/profile` | Get user details |
| `PUT` | `/api/user/profile` | Update user details |
| `GET` | `/api/tasks` | Get all tasks (supports `search`, `completed`, `date` query params) |
| `POST` | `/api/tasks` | Create a new task (optional `dueDate`) |
| `PUT` | `/api/tasks/:id` | Toggle completion or edit task |
| `DELETE` | `/api/tasks/:id` | Delete a task |
| `GET` | `/api/health` | Simple health check (no auth) |

> **Authentication** – All task routes require the `Authorization: Bearer <token>` header.

---

## 🎨 Screenshots

*(Add screenshots of the UI here – e.g., login page, dashboard, task list)*

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/awesome-feature`).
3. Commit your changes with clear messages.
4. Open a Pull Request describing the changes.

Please ensure your code adheres to the existing style (ESLint + Prettier).

---

## 📄 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- **Vercel** for the Next.js framework.
- **MongoDB** for the flexible NoSQL database.
- **Heroicons** for beautiful SVG icons.

Feel free to open an issue for bugs or feature requests. Happy coding! 🚀

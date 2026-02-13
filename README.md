# ClassConnect – MERN Stack Learning Management System

ClassConnect is a full‑stack **Learning Management System (LMS)** built with the **MERN stack**  
(**MongoDB, Express.js, React.js, Node.js**). It connects **instructors** and **students** on a single platform where instructors can create and manage courses with video lectures, and students can enroll and learn at their own pace.

---

## ✨ Features

### Authentication & Roles
- User registration and login using email and password
- Secure password storage with hashing (e.g., bcrypt)
- Role‑based access: **Student** and **Instructor**
- Profile page with avatar, bio, role, and email

### Instructor Features
- Instructor dashboard with quick stats
- Create, edit, and delete courses
- Add detailed course information:
  - Title, subtitle, description
  - Category, level (Beginner / Medium / Advance)
  - Course price (INR)
  - Course thumbnail
- Add, edit, and remove lectures with:
  - Lecture title
  - Video URL
  - Public ID (for cloud storage)
  - Free preview flag
- Publish / Unpublish courses
- View enrolled students per course (via DB / reports)

### Student Features
- Browse all **published** courses
- View course details and preview lectures
- Enroll into courses
- Dashboard with:
  - Enrolled courses
  - Basic activity stats (e.g., active courses, upcoming deadlines placeholder)
- Watch course lectures from inside the app

### Under the Hood
- RESTful API using **Express + Node**
- MongoDB data modeling with **Mongoose**
- Clean, responsive UI built with **React** (SPA)
- Role‑based route protection on frontend and backend
- Reusable components for forms, cards, dashboards

---

## 🏗️ Tech Stack

**Frontend**
- React
- React Router
- CSS framework / custom styling (Tailwind / custom)
- ShadCN UI library

**Backend**
- Node.js
- Express.js
- Mongoose (MongoDB ODM)
- JSON Web Tokens (JWT) for auth (recommended)

**Database**
- MongoDB

---

## 📁 Project Structure (example)

## 🧱 Project Structure

The project is organized as a monorepo with separate **backend** (Node/Express API) and **frontend** (React) apps.

```bash
ClassConnect/
├── backend/                    # Node.js + Express server
│   ├── controllers/            # Route handlers / business logic
│   ├── middleware/             # Auth, error handling, etc.
│   ├── models/                 # Mongoose models (User, Course, Lecture)
│   ├── routes/                 # Express route definitions (auth, courses, lectures)
│   ├── utils/                  # Reusable helpers (e.g. tokens, validators)
│   ├── node_modules/
│   ├── .env                    # Backend environment variables (Mongo URI, JWT secret, etc.)
│   ├── index.js                # Entry point for the backend server
│   ├── package.json
│   └── package-lock.json
│
├── frontend/                   # React client application
│   ├── public/                 # Static files (index.html, favicons, etc.)
│   ├── src/
│   │   ├── assets/             # Images, icons, static assets
│   │   ├── components/         # Reusable UI components
│   │   ├── lib/                # API wrappers, utilities, config
│   │   ├── pages/              # Page-level components mapped to routes
│   │   ├── redux/              # Redux store, slices, actions
│   │   ├── App.jsx             # Root app component / routes
│   │   ├── index.css           # Global styles
│   │   └── main.jsx            # React entry point (renders App to DOM)
│   ├── node_modules/
│   ├── .env                    # Frontend environment variables (API base URL, etc.)
│   ├── package.json
│   └── package-lock.json
│
└── README.md                   # Project documentation
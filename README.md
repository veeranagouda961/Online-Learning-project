# 🎓 LMS (Learning Management System)

A full-stack Learning Management System (LMS) that allows users to browse courses, enroll, watch YouTube-based lessons, and track their progress.

---

## 🚀 Project Overview

This LMS platform enables structured learning using YouTube videos. It provides:

* Course browsing and enrollment
* Video-based lesson playback
* Progress tracking
* Authentication with JWT
* Resume learning from last watched lesson

> Videos are not stored in the system — only YouTube URLs are used, making the system lightweight and scalable.

---

## 🛠️ Tech Stack

### Frontend

* React (Vite)
* Tailwind CSS
* Axios

### Backend

* Node.js
* Express.js

### Database

* MongoDB (Mongoose)

### Authentication

* JWT (JSON Web Tokens)

---

## ✨ Features

### 👨‍🎓 Student Features

* Browse available courses
* View course details
* Enroll in courses
* Watch lessons via YouTube embed
* Track progress automatically
* Resume last watched lesson

### 🔐 Authentication

* Signup & Login
* JWT-based authentication
* Protected routes

### 📊 Progress Tracking

* Tracks completed lessons
* Calculates completion percentage
* Saves last watched lesson

---

## 📁 Project Structure

```
LMS/
├── client/         # React frontend
├── server/         # Node.js backend
│   ├── src/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── middleware/
│   │   └── index.js
│   ├── seed.js
│   └── .env
```

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository

```
git clone <your-repo-url>
cd LMS
```

---

### 2️⃣ Backend Setup

```
cd server
npm install
```

Create a `.env` file inside `server/`:

```
MONGODB_URI=mongodb://127.0.0.1:27017/lms
PORT=5000
JWT_SECRET=your_secret_key
```

---

### 3️⃣ Seed Demo Data (IMPORTANT)

```
node seed.js
```

This will create:

* 1+ courses
* Sections
* Lessons with YouTube videos

---

### 4️⃣ Start Backend

```
npm run dev
```

Backend runs at:

```
http://localhost:5000
```

---

### 5️⃣ Frontend Setup

Open new terminal:

```
cd client
npm install
npm run dev
```

Frontend runs at:

```
http://localhost:5173
```

---

## 🔗 API Endpoints

### Courses

* `GET /api/courses`
* `GET /api/courses/:id`
* `GET /api/lessons/:courseId`

### Enrollment

* `POST /api/enroll`

### Progress

* `POST /api/progress`
* `GET /api/progress/:courseId`

### Authentication

* `POST /api/auth/signup`
* `POST /api/auth/login`
* `GET /api/auth/me`

---

## 🧠 How It Works

1. User logs in
2. Fetches courses from backend
3. Selects a course → lessons loaded
4. YouTube video is embedded using iframe
5. When video ends → progress is saved
6. Backend calculates completion percentage

---

## ⚠️ Important Notes

* Videos are NOT stored in the database
* Only YouTube URLs are saved
* Backend controls lesson order and structure
* Frontend only renders data

---

## 🚀 Future Improvements

* Admin dashboard (add/edit courses)
* Course categories & search
* Ratings & reviews
* Certificates on completion
* Payment integration

---

## 📸 Screenshots

*Add your project screenshots here*

---

## 👨‍💻 Author

**Veeresh**

---

## 📄 License

This project is for learning and demonstration purposes.
# Online-Learning-project

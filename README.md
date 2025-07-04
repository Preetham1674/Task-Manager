# TaskScheduler

## 🚀 Overview

TaskScheduler is a comprehensive, web-based MERN stack application designed to streamline personal and team productivity. It offers an intuitive platform for efficient task creation, prioritization, tracking, and timely reminders, aiming to bring order to your daily commitments and boost overall efficiency.

## ✨ Features

- **User Authentication:** Secure user registration, login, and logout functionalities using JSON Web Tokens (JWT).
- **Task Management (CRUD):**
  - **Create:** Easily add new tasks with titles, descriptions, due dates, and priorities.
  - **Read:** View all tasks associated with your authenticated user account.
  - **Update:** Modify existing task details and priorities.
  - **Delete:** Remove tasks when they are no longer needed.
- **Task Status Tracking:** Mark tasks as "Completed" or "Pending" to track your progress.
- **Personalized Reminders:**
  - Client-side browser alerts for immediate notifications.
  - Server-side email notifications for scheduled reminders (requires email service setup).
- **Intuitive UI/UX:** A responsive and visually appealing interface designed for ease of use.
- **Data Segregation:** Ensures each user can only access and manage their own tasks.

## 🛠️ Tech Stack

**Frontend:**

- **ReactJS:** A JavaScript library for building user interfaces.
- **React Router DOM:** For declarative client-side routing within the Single Page Application (SPA).
- **Axios:** A promise-based HTTP client for making API requests.
- **date-fns:** A modern JavaScript date utility library.
- **CSS:** Modular and component-specific styling (`.css` files).

**Backend:**

- **Node.js:** JavaScript runtime environment.
- **Express.js:** Fast, unopinionated, minimalist web framework for Node.js.
- **MongoDB:** NoSQL document database for flexible data storage.
- **Mongoose:** MongoDB object data modeling (ODM) library for Node.js.
- **jsonwebtoken:** For implementing JSON Web Tokens (JWT) for secure authentication.
- **bcryptjs:** For hashing and salting passwords securely.
- **node-cron:** For scheduling server-side tasks (e.g., reminder checks).
- **moment-timezone:** For handling timezones in server-side reminders.
- **Nodemailer:** For sending email notifications from the backend.
- **CORS:** Express middleware to enable Cross-Origin Resource Sharing.
- **dotenv:** For managing environment variables.

## 🏛️ Architecture

TaskScheduler follows a classic **Client-Server architecture** with a **RESTful API**.

- **Frontend (ReactJS):** Serves as a Single Page Application (SPA) handling user interaction and making asynchronous API calls to the backend.
- **Backend (Node.js/Express.js):** Provides a RESTful API for authentication and task management. It processes requests, interacts with the database, and manages server-side logic, including scheduled reminder checks.
- **Database (MongoDB):** A NoSQL database that stores all user and task data, connected to the backend via Mongoose.
- **Communication:** Frontend and Backend communicate primarily using HTTP/HTTPS requests with JSON payloads. JWTs are used for authentication for all protected API routes.

### Prerequisites

- Node.js
- npm (Node Package Manager)
- MongoDB Community Server (running locally) or access to a MongoDB Atlas cluster.
- Git

### Using the Application

1.  **Register:** Create a new user account on the `/register` page.
2.  **Login:** Use your newly created credentials to log in.
3.  **Manage Tasks:** Once logged in, you can create, view, edit, delete, and mark tasks as complete on the `/tasks` page.
4.  **Test Reminders:** Create a task with a reminder set a few minutes in the future. Keep the tasks page open to see browser alerts, or check the `EMAIL_USER`'s inbox for email reminders (if correctly configured).

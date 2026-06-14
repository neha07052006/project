# Store Rating System

## Project Overview

Store Rating System is a full-stack web application that allows users to rate stores, store owners to monitor ratings for their stores, and administrators to manage users and stores through a role-based access control system.

The application supports three types of users:

* Admin
* Normal User
* Store Owner

---

## Features

### Admin

* Login securely
* View dashboard statistics

  * Total Users
  * Total Stores
  * Total Ratings
* Add new users
* Add new stores
* View all users
* Search and filter users by role
* View user details
* View all stores

### User

* Register account
* Login securely
* View available stores
* Submit ratings (1–5)
* Update password

### Store Owner

* Login securely
* View store dashboard
* View average store rating
* View users who have rated their store
* Update password

---

## Technology Stack

### Frontend

* React.js
* React Router DOM
* Axios
* Bootstrap 5

### Backend

* Node.js
* Express.js
* JWT Authentication
* bcrypt Password Hashing

### Database

* MySQL

---

## Project Structure

```text
StoreRatingSystem
│
├── backend
│   ├── config
│   ├── controllers
│   ├── middleware
│   ├── routes
│   ├── utils
│   └── server.js
│
├── frontend
│   ├── src
│   │   ├── components
│   │   ├── pages
│   │   ├── services
│   │   └── App.jsx
│
├── database.sql
└── README.md
```

---

## Installation and Setup

### 1. Clone Repository

```bash
git clone <repository-url>
cd StoreRatingSystem
```

---

### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file inside the backend folder:

```env
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=store_rating_system
JWT_SECRET=your_secret_key
```

Start backend server:

```bash
npm start
```

---

### 3. Database Setup

Create a MySQL database:

```sql
CREATE DATABASE store_rating_system;
```

Import the provided `database.sql` file into MySQL.

---

### 4. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

Frontend will start on:

```text
http://localhost:5173
```

---

## Authentication & Security

* JWT-based Authentication
* Passwords encrypted using bcrypt
* Role-Based Access Control
* Protected API Routes

---

## Roles and Permissions

| Feature             | Admin | User | Store Owner |
| ------------------- | ----- | ---- | ----------- |
| Login               | ✓     | ✓    | ✓           |
| Change Password     | ✓     | ✓    | ✓           |
| Add User            | ✓     | ✗    | ✗           |
| Add Store           | ✓     | ✗    | ✗           |
| View Users          | ✓     | ✗    | ✗           |
| View Stores         | ✓     | ✓    | ✗           |
| Submit Rating       | ✗     | ✓    | ✗           |
| View Average Rating | ✗     | ✗    | ✓           |
| View User Ratings   | ✗     | ✗    | ✓           |

---

## Future Improvements

* Owner selection dropdown while creating stores
* Pagination for large datasets
* Email verification
* Forgot Password functionality
* Profile management
* Store images and categories

---

## Author

**Shashwat Gole**

Full Stack Developer Intern Coding Challenge Submission

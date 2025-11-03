# College PathFinder

> A comprehensive educational search and recommendation platform to help students find suitable colleges based on their All India Rank (AIR) and preferences.

**CS253 Course Project** - 2nd Semester 2023-2024  
**Instructor:** Prof. Indranil Saha, IIT Kanpur

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [Deployment](#deployment)
- [Documentation](#documentation)

## 🎯 About

College PathFinder is a full-stack web application designed to streamline the college selection process for students. The platform provides intelligent college recommendations based on All India Rank (AIR) and various other criteria, helping students make informed decisions about their higher education.

## ✨ Features

- **College Search & Filter**: Search and filter colleges based on multiple criteria
- **College Comparison**: Side-by-side comparison of different colleges
- **College Predictor**: Get college recommendations based on your AIR
- **User Authentication**: Secure registration and login with OTP verification
- **User Dashboard**: Personalized dashboard for verified users
- **Community Features**: 
  - Create and view posts
  - Reply to discussions
  - Tag-based organization
- **User Profiles**: Manage your profile and preferences

## 🛠 Technology Stack

### Frontend
- **React.js** (v18.2.0) - UI framework
- **React Router** (v5.2.0) - Client-side routing
- **React Bootstrap** - UI components
- **Axios** - HTTP client
- **JWT Decode** - Token management

### Backend
- **Node.js** - Runtime environment
- **Express.js** (v4.17.1) - Web framework
- **MongoDB** - Database
- **Mongoose** (v5.11.8) - ODM
- **JWT** - Authentication
- **Nodemailer** - Email service for OTP
- **Bcrypt** - Password hashing

### Deployment
- **Frontend**: Vercel
- **Backend**: Render.com
- **Database**: MongoDB Atlas

## 📁 Project Structure

```
CS253-Project/
├── college_frontend-main/     # React frontend application
│   ├── src/
│   │   ├── components/        # React components
│   │   ├── services/          # API services
│   │   └── utils/             # Utility functions
│   └── package.json
├── college_backend-main/      # Express backend API
│   ├── routes/                # API routes
│   ├── models/                # Database models
│   ├── middleware/            # Custom middleware
│   ├── config/                # Configuration files
│   └── package.json
├── Software_Design_Documents/
├── Software_Implementation_Documents/
├── Software_Requirement_Specifiaction_Documents/
├── Software_Test_Documents/
├── Software_User_Manual/
└── README.md
```

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14.x or higher)
- **npm** (v6.x or higher)
- **MongoDB** (for local development) or MongoDB Atlas account
- **Web Browser** (Chrome, Firefox, Safari, or Edge)

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/SmartCheese22/CS253-Project.git
cd CS253-Project
```

### 2. Install Frontend Dependencies

```bash
cd college_frontend-main
npm install --force
```

### 3. Install Backend Dependencies

```bash
cd ../college_backend-main
npm install --force
```

> **Note**: If you encounter errors with bcrypt during installation, run:
> ```bash
> npm uninstall bcrypt
> npm install bcrypt
> ```

## ⚙️ Configuration

### Backend Configuration

Create a `.env` file in the `college_backend-main` directory with the following variables:

```env
jwtPrivateKey=your_jwt_private_key_here
MAIL_USER=your_email@example.com
MAIL_PASS=your_email_password_or_app_password
mongoDBURL=your_mongodb_connection_string
PORT=5000
```

**Configuration Details:**
- `jwtPrivateKey`: Secret key for JWT token generation
- `MAIL_USER`: Email address for sending OTP emails
- `MAIL_PASS`: Password or app-specific password for the email account
- `mongoDBURL`: MongoDB connection string (local or Atlas)
- `PORT`: Port number for the backend server (default: 5000)

## 🏃 Running the Application

### Start the Backend Server

```bash
cd college_backend-main
npm start
```

The backend API will be available at `http://localhost:5000/`

For development with auto-reload:
```bash
npm run dev
```

### Start the Frontend Application

```bash
cd college_frontend-main
npm start
```

The frontend will automatically open in your browser at `http://localhost:3000/`

If it doesn't open automatically, navigate to `http://localhost:3000/` manually.

## 🌐 Deployment

The application is deployed and accessible online:

- **Frontend**: Deployed on [Vercel](https://vercel.com)
- **Backend**: Deployed on [Render.com](https://render.com)
- **Database**: Hosted on [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)

## 📚 Documentation

Comprehensive project documentation is available in the following directories:

- **Software Requirements Specification (SRS)**: `Software_Requirement_Specifiaction_Documents/`
- **Software Design Document (SDD)**: `Software_Design_Documents/`
- **Software Implementation Document (SID)**: `Software_Implementation_Documents/`
- **Software Test Document (STD)**: `Software_Test_Documents/`
- **User Manual**: `Software_User_Manual/`

Each directory contains versioned PDF documents (v1 and v2).

## 📝 API Endpoints

### User Routes (`/users`)
- User registration and login
- User profile management
- OTP verification

### Post Routes (`/posts`)
- Create, read, update, delete posts
- Search and filter posts

### Reply Routes (`/reply`)
- Add replies to posts
- Manage discussions

### Tag Routes (`/tags`)
- Tag management for categorizing posts

### OTP Routes (`/otp`)
- OTP generation and verification

---

**Course**: CS253 - Software Development and Operations  
**Institution**: Indian Institute of Technology, Kanpur  
**Academic Year**: 2023-2024

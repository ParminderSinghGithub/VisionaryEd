# VisionaryEd

**VisionaryEd** is a dynamic web platform designed to simplify access to crucial information about the **Indian Institutes of Technology (IITs)**. Built using the **MERN stack** (MongoDB, Express.js, React, and Node.js), VisionaryEd serves as a centralized hub for aspiring students to access key details such as **cutoffs, exam dates, and official links** to IIT websites. The platform aims to streamline the often overwhelming process of gathering information from multiple sources.

---

## Table of Contents
1. [Introduction](#introduction)
2. [Problem Statement](#problem-statement)
3. [Solution Overview](#solution-overview)
4. [Features](#features)
5. [Technologies Used](#technologies-used)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Developer Information](#developer-information)

---

## Introduction
VisionaryEd is a **user-friendly web platform** that provides aspiring students with a **centralized resource** for accessing information about IITs. The platform leverages the **MERN stack** to deliver a seamless and interactive experience, making it easier for students to navigate through crucial details like cutoffs, exam dates, and official IIT websites.

---

## Problem Statement
Aspiring students often face challenges in navigating the **excessive and scattered information** available about IITs. This includes details like **cutoffs, exam dates, and admission procedures**, which are spread across multiple platforms. VisionaryEd addresses this issue by **centralizing all relevant information** in one place, simplifying the process for students.

---

## Solution Overview
VisionaryEd offers the following key functionalities:
1. **Seamless Registration and Login**: A simple and secure process for users to register and log in.
2. **Personalized Welcome Emails**: Automated emails sent to users upon successful registration.
3. **Cutoff Details**: A user-friendly form to access cutoff details of the **top 7 IITs**.
4. **Direct Links to IIT Websites**: Quick access to official IIT websites for further exploration.
5. **Event Calendar**: A calendar highlighting important dates and exam details for IIT admissions.

---

## Features
- **User Registration**: Intuitive and straightforward registration process.
- **Welcome Email**: Automated email sent to users after registration.
- **Secure Login**: A robust authentication mechanism for secure access.
- **IIT Cutoffs Form**: A form to retrieve cutoff details of the top 7 IITs.
- **Official IIT Links**: Direct links to the official websites of IITs.
- **Event Calendar**: Displays important dates and exam-related information.

---

## Technologies Used
- **Frontend**: React (for dynamic and interactive user interfaces)
- **Backend**: Node.js and Express.js (for server-side scripting and handling HTTP requests)
- **Database**: MongoDB (for efficient data storage and retrieval)
- **Authentication**: Secure login and registration system
- **APIs**: Fetch API (for seamless communication between frontend and backend)

---

## Installation
To set up VisionaryEd locally, follow these steps:

### Prerequisites
- **Node.js**: Ensure Node.js (v16 or higher) is installed on your system.
- **MongoDB**: Use MongoDB Atlas (cloud-based service - recommended) or install MongoDB locally.
- **Gmail Account**: For email functionality, you'll need a Gmail account with app-specific password enabled.

### Step 1: Clone the Repository
```bash
git clone https://github.com/ParminderSinghGithub/VisionaryEd.git
cd VisionaryEd
```

### Step 2: Install Backend Dependencies
Navigate to the backend directory and install dependencies:
```bash
cd Server
npm install
```

### Step 3: Set Up Environment Variables for Backend
Create a `.env` file in the `Server` directory with the following variables:
```
PORT=5000
MONGO_URI=mongodb+srv://username:password@clustername.mongodb.net/visionaryed?retryWrites=true&w=majority
EMAIL_USER=your_gmail_email@gmail.com
EMAIL_PASS=your_16_digit_app_password
SENDER_NAME=VisionaryEd
SENDER_EMAIL=your_gmail_email@gmail.com
```

**Important Notes:**
- **MONGO_URI**: Replace with your MongoDB Atlas connection string (includes username, password, and cluster name). The database name `visionaryed` should be included at the end.
- **EMAIL_USER** and **SENDER_EMAIL**: Use your Gmail email address.
- **EMAIL_PASS**: This is NOT your regular Gmail password. Generate an **App-Specific Password** by:
  1. Going to https://myaccount.google.com/security
  2. Enabling 2-Step Verification (if not already enabled)
  3. Generating an "App Password" for Mail/Windows
  4. Copy the 16-digit password and paste it as EMAIL_PASS

### Step 4: Start the Backend Server
Run the backend server using one of these commands:
```bash
# Option 1: Using Node directly
node server.js

# Option 2: Using Nodemon for development (auto-restart on file changes)
npx nodemon server.js
```
The backend will start running on `http://localhost:5000`.

### Step 5: Install Frontend Dependencies
Open a new terminal, navigate to the frontend directory, and install dependencies:
```bash
cd ../Client
npm install
```

### Step 6: Start the Frontend Application
Run the frontend application using:
```bash
npm run dev
```
The frontend will start running on `http://localhost:3001`.

--- 

## Usage

### For Students:
1. **Register**: Click on the "Sign Up" button and provide your name, email, and password.
2. **Receive Welcome Email**: You'll automatically receive a welcome email at your registered email address.
3. **Login**: Use your email and password to log in to the platform.
4. **Explore IIT Information**:
   - Navigate to the **Colleges** section to view cutoff details for top IITs.
   - Filter by Institute, Academic Program, Quota, Seat Type, and Gender to find relevant information.
   - Click on institute links to visit their official websites.
5. **Check Event Calendar**: View important exam dates and admission deadlines in the Event Calendar.
6. **Browse FAQs**: Get answers to common questions about IIT admissions and the platform.

### For Educators:
Use the platform to guide students with accurate and centralized information about IIT admissions, cutoffs, and important dates.

---

## Troubleshooting

### Common Issues:

**1. Backend server won't start**
- Ensure MongoDB connection string is correct in `.env`
- Check if port 5000 is already in use: `netstat -an | findstr :5000` (Windows)
- Verify all environment variables are set in `.env`

**2. Emails not sending**
- Verify EMAIL_USER is your full Gmail address
- Ensure EMAIL_PASS is the 16-digit app-specific password (not your regular Gmail password)
- Check if 2-Step Verification is enabled on your Gmail account
- Look for SMTP errors in the backend console

**3. Frontend won't start**
- Delete `node_modules` and `package-lock.json`, then run `npm install` again
- Ensure Node.js version is v16 or higher: `node --version`
- Check if port 3001 is already in use

**4. MongoDB connection errors**
- Verify the connection string includes your username and password
- Check IP address whitelist in MongoDB Atlas (allow 0.0.0.0/0 for development)
- Ensure the database name is included in the connection string

---

## Deployment

Recommended setup:
- **Frontend**: Vercel
- **Backend**: Render
- **Database**: MongoDB Atlas

### Backend on Render
1. Create a new Render Web Service from the `Server` folder.
2. Set the build/start command to use the backend scripts.
3. Add these environment variables in Render:
  - `MONGO_URI`
  - `EMAIL_USER`
  - `EMAIL_PASS`
  - `SENDER_NAME`
  - `SENDER_EMAIL`
  - `CLIENT_URLS` = your Vercel frontend URL, plus `http://localhost:3001` for local testing if needed
4. Use the `/health` endpoint for a quick uptime check.

### Frontend on Vercel
1. Create a new Vercel project from the `Client` folder.
2. Set `VITE_API_BASE_URL` to your Render backend URL.
3. Keep the default Vercel build output from Vite.
4. The `Client/vercel.json` rewrite keeps React Router routes working.

### Example frontend env
```bash
VITE_API_BASE_URL=https://your-render-service.onrender.com
```

--- 

## Developer Information
Parminder Singh  
GitHub: https://github.com/ParminderSinghGithub

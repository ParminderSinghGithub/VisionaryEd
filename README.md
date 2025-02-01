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
- **Node.js**: Ensure Node.js is installed on your system.
- **MongoDB**: Install MongoDB locally or use a cloud-based MongoDB service.

### Step 1: Clone the Repository
```
git clone https://github.com/ParminderSinghGithub/VisionaryEd.git
cd VisionaryEd
```
### Step 2: Install Backend Dependencies
Navigate to the backend directory and install dependencies:
```
cd Server
npm install
```
### Step 3: Set Up Environment Variables for Backend
Create a .env file in the backend directory and add the following variables:
```
PORT=5000
MONGO_URI=your_mongodb_connection_string
EMAIL_USER=your_email_address
EMAIL_PASS=your_email_password
JWT_SECRET=your_jwt_secret_key
```
### Step 4: Start the Backend Server
Run the backend server using the following command:
```
node server.js
```
The backend will start running on http://localhost:5000.

### Step 5: Install Frontend Dependencies
Open a new terminal, navigate to the frontend directory, and install dependencies:
```
cd ../Client
npm install
```
### Step 6: Start the Frontend Application
Run the frontend application using:
```
npm start
```
The frontend will start running on http://localhost:3000.

--- 

## Usage
**Students**: Register, log in, and explore cutoff details, exam dates, and official IIT links.  
**Educators**: Use the platform to guide students with accurate and centralized information.

--- 

## Developer Information
Parminder Singh  
GitHub: https://github.com/ParminderSinghGithub

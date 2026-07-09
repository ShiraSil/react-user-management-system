# React Users Management System

> “The system is based on a local JSON Server (fake REST API), so some functionality is not available in the GitHub Pages environment due to the lack of an active backend server. In the local development environment, all services run normally.”

## Overview

A full-featured React SPA that simulates a real-world user management system using a local JSON Server as a REST API backend.

The project is based on a structured dataset similar to JSONPlaceholder and demonstrates advanced frontend development practices including authentication, routing, state management, and asynchronous data handling.

## Collaborators

This project was developed as a collaborative effort by:

- **Shira Silberman** - [GitHub](https://github.com/shirasil)
- **Chana Belenson** - [GitHub](https://github.com/chanabelenson)

## Tech Stack

![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white) ![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white) ![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white) ![JSON](https://img.shields.io/badge/json-5E5E5E?style=for-the-badge&logo=json&logoColor=white)

**React Router v6** · **Fetch API** · **React Hooks** · **Context API** · **Async/Await** · **Custom Hooks**

## Core Features

- **Authentication System:** Login and registration flow with persistent session storage.
- **User Dashboard:** Central hub with navigation to user-related data and actions.
- **Todos Management:** Full CRUD operations with filtering, sorting, and status tracking.
- **Posts & Comments:** Create, edit, and delete posts with nested comments support and user-based permissions.
- **Albums & Photos:** Dynamic album browsing with incremental photo loading and full media management.

## Architecture Highlights

- Modular component-based structure
- Global state management using Context API
- Protected routing with React Router v6
- Optimized API calls and client-side data handling
- Reusable custom hooks for logic separation

## Project Goal

To simulate a scalable frontend system working with REST APIs, while applying modern React patterns and best practices in real application architecture.

---

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Make sure you have **Node.js** (v18 or higher) and **npm** installed on your machine. You can download it from [nodejs.org](https://nodejs.org/).

### Installation & Local Setup

1. **Clone the repository:**
   Run the following commands in your terminal to clone the project and navigate into the root directory:

   **git clone [https://github.com/shirasil/react-users-management-system.git](https://github.com/shirasil/react-users-management-system.git)**

   **cd react-users-management-system**

2. **Setup the Client (Frontend):**
   Navigate to the client directory and install the required dependencies:

   **cd client**

   **npm install**

3. **Setup the Server (Backend):**
   Open a new terminal window or tab, navigate to the server directory, and ensure your db.json file is present.

---

## Running the Application

To run the full-stack application locally, you need to start **both** the frontend and the mock backend server simultaneously.

### 1. Start the Backend Server

In your server terminal window, run the following commands to start the JSON Server on port 3002:

**cd server**

**npx json-server --watch db.json --port 3002**

_Verify it's running by visiting: http://localhost:3002/users_

### 2. Start the Frontend Application

In your client terminal window, run the development server:

**cd client**

**npm run dev**

_Open your browser and navigate to the local address provided by Vite (typically http://localhost:5173)._

---

## Authentication & Login Credentials

Since this application utilizes a local JSON Server with a dataset structured like JSONPlaceholder, authorized system users are managed directly within the backend database.

To log into the system, use any user record available in your db.json file under the users array using the following mapping:

- **Username:** Use the "username" field value (e.g., Bret).
- **Password:** Use the "website" field value (e.g., anastasia.net).

> 📌 **Note:** Any modifications made during the session (such as creating new tasks or posts) will be written directly to your local db.json file.

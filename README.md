# React Users Management System

**[Click here to view the live deployment](https://shirasil.github.io/react-users-management-system/)**

> “The system is based on a local JSON Server (fake REST API), so some functionality is not available in the GitHub Pages environment due to the lack of an active backend server. In the local development environment, all services run normally.”

## Overview

A full-featured React SPA that simulates a real-world user management system using a local JSON Server as a REST API backend.

The project is based on a structured dataset similar to JSONPlaceholder and demonstrates advanced frontend development practices including authentication, routing, state management, and asynchronous data handling.

## Application Preview

<details>
<summary>Click here to view screenshots of the app.</summary>

### Login Page
<img width="956" height="906" alt="Login Page" src="https://github.com/user-attachments/assets/e47cb1bd-43df-4ec4-9dbb-02eac4142b22" />

### Home Page
<img width="1352" height="905" alt="Home Page" src="https://github.com/user-attachments/assets/2f2b53d8-347a-4968-87dd-bd560ae85ead" />

### Todos Page
<img width="1430" height="860" alt="Todos Page" src="https://github.com/user-attachments/assets/108e506d-6bf3-4759-9b3e-2a0e37f0f0b0" />

### Album Photos View
<img width="1197" height="906" alt="Album Photos View" src="https://github.com/user-attachments/assets/6830a1b3-c9e4-4907-9723-d07b4be90ec4" />

</details>

## Collaborators

This project was developed as a collaborative effort by:

- **Shira Silberman** - [GitHub](https://github.com/ShiraSil)
- **Chana Belenson** - [GitHub](https://github.com/chanabelenson)

## Tech Stack

![React](https://img.shields.io/badge/React-19-%2320232a.svg?style=flat&logo=react&logoColor=%2361DAFB) ![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-%23323330.svg?style=flat&logo=javascript&logoColor=%23F7DF1E) ![React Router](https://img.shields.io/badge/React_Router-v6-CA4245?style=flat&logo=react-router&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-8-%23646CFF.svg?style=flat&logo=vite&logoColor=white) ![NodeJS](https://img.shields.io/badge/Node.js-Express-6DA55F?style=flat&logo=node.js&logoColor=white) ![JSON](https://img.shields.io/badge/JSON_Server-Mock_API-5E5E5E?style=flat&logo=json&logoColor=white) ![Fetch API](https://img.shields.io/badge/Fetch_API-Async_Data-007ACC?style=flat) ![React Hooks](https://img.shields.io/badge/React_Hooks-Custom_&_Built_in-61DAFB?style=flat&logo=react&logoColor=black) ![Context API](https://img.shields.io/badge/Context_API-State_Management-purple?style=flat) ![Custom Hooks](https://img.shields.io/badge/Custom_Hooks-Logic_Separation-orange?style=flat) ![Async/Await](https://img.shields.io/badge/Async%2FAwait-Promises-success?style=flat)

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

## Project Structure

```text
├── client/
│   ├── public/         # Static assets & favicons
│   └── src/
│       ├── components/ # Global reusable UI components
│       ├── features/   # Feature-based modules
│       │   ├── albums/ # Albums pages and logic
│       │   ├── auth/   # Authentication, Login, and AuthContext
│       │   ├── posts/  # Posts & Comments management
│       │   ├── shared/ # Shared custom hooks and components
│       │   └── todos/  # Todos CRUD operations & caching
│       ├── styles/     # Global application styles
│       └── main.jsx    # Application entry point
└── server/
    └── db.json         # Mock REST API database
```

---

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Make sure you have **Node.js** (v18 or higher) and **npm** installed on your machine. You can download it from [nodejs.org](https://nodejs.org/).

### Installation & Local Setup

1. **Clone the repository:**
  Run the following commands in your terminal to clone the project and navigate into the root directory:

```bash
   git clone https://github.com/ShiraSil/react-users-management-system.git
   cd react-users-management-system
```

2. **Setup the Client (Frontend):**
   Navigate to the client directory and install the required dependencies:

```bash
   cd client
   npm install
```

3. **Setup the Server (Backend):**
Open a new terminal window, navigate to the server directory, and install dependencies:

```bash
   cd server
   npm install
```

## Environment Configuration

This project uses Vite environment files to automatically handle API endpoints:
- **Development:** Connects to `http://localhost:3002` (via `.env.development`).
- **Production:** Connects to the deployed Render server (via `.env.production`).

No manual configuration changes are required when switching environments.

---

## Running the Application

To run the full-stack application locally, you need to start **both** the frontend and the mock backend server simultaneously.

### 1. Start the Backend Server

In your server terminal window, run the following commands to start the JSON Server on port 3002:

```bash
cd server
npx json-server --watch db.json --port 3002
```

_Verify it's running by visiting: http://localhost:3002/users_

### 2. Start the Frontend Application

In your client terminal window, run the development server:

```bash
cd client
npm run dev
```

_Open your browser and navigate to the local address provided by Vite (typically http://localhost:5173/react-users-management-system/)._

---

## Authentication & Login Credentials

Since this application utilizes a local JSON Server with a dataset structured like JSONPlaceholder, authorized system users are managed directly within the backend database.

To log into the system, use any user record available in your db.json file under the users array using the following mapping:

- **Username:** Use the "username" field value (e.g., Danielc).
- **Password:** Use the "website" field value (e.g., danielcohen.dev).

> 📌 **Note:** Any modifications made during the session (such as creating new tasks or posts) will be written directly to your local db.json file.

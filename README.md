# 💬 Chatty - Modern Fullstack Chat Application

![Chatty Dashboard Banner](frontend/public/banner1.png)

> _A sleek, glassmorphic real-time chat dashboard delivering a premium communication experience._

[![React](https://img.shields.io/badge/React-18.3-61DAFB?style=for-the-badge&logo=react)](https://react.dev/)
[![Node.js](https://img.shields.io/badge/Node.js-20.x-339933?style=for-the-badge&logo=nodedotjs)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.21-000000?style=for-the-badge&logo=express)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-8.8-47A248?style=for-the-badge&logo=mongodb)](https://www.mongodb.com/)
[![Socket.io](https://img.shields.io/badge/Socket.io-4.8-010101?style=for-the-badge&logo=socketdotio)](https://socket.io/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)

---

## 🌟 Overview

**Chatty** is a state-of-the-art real-time messaging application built to demonstrate modern fullstack capabilities. It combines seamless WebSocket communication with a beautiful, responsive interface featuring **glassmorphism**, **dynamic themes**, and smooth interactions. Whether you're connecting with friends or colleagues, Chatty provides a premium chat experience.

## ✨ Key Features

- **🎨 Modern Glassmorphic Design**: A visually stunning UI with frosted glass components, dynamic background patterns, and vibrant gradients.
- **⚡ Real-Time Messaging**: Powered by **Socket.io** for instant message delivery and online status tracking.
- **🔐 Secure Authentication**:
  - Robust user authentication using **JWT** and **HttpOnly cookies**.
  - Secure password hashing with **bcryptjs**.
- **�️ Profile & Image Uploads**:
  - Integrated with **Cloudinary** for seamless image hosting and avatar management.
- **🎭 Dynamic Themes**: Choose from **32+ built-in themes** powered by DaisyUI, with preference persistence.
- **📱 Responsive Layout**: Fully optimized for all devices, from desktop dashboards to mobile screens.
- **� Interactive UI**: Real-time notifications and toast alerts using **React Hot Toast**.

---

## 🛠️ Tech Stack & Libraries

Built with the latest and greatest in the JavaScript ecosystem:

### Frontend

| Category       | Technology           | Usage                                                          |
| :------------- | :------------------- | :------------------------------------------------------------- |
| **Core**       | **React 18**         | Modern component-based architecture with Hooks.                |
| **Build Tool** | **Vite 5**           | Blazing fast development server and optimized builds.          |
| **Styling**    | **Tailwind CSS 3**   | Utility-first CSS with custom configuration for glass effects. |
| **UI Library** | **DaisyUI 4**        | Accessible component library with extensive theme support.     |
| **State/Data** | **Zustand**          | Lightweight and powerful state management.                     |
| **Real-time**  | **Socket.io Client** | Persistent WebSocket connection for instant chat.              |
| **Icons**      | **Lucide React**     | Consistent, lightweight SVG icons.                             |

### Backend

| Category       | Technology            | Usage                                                    |
| :------------- | :-------------------- | :------------------------------------------------------- |
| **Server**     | **Node.js / Express** | Robust and scalable backend server.                      |
| **Database**   | **MongoDB**           | NoSQL database for flexible data storage (via Mongoose). |
| **Auth**       | **JWT**               | Industry standard JSON Web Token based authentication.   |
| **Storage**    | **Cloudinary**        | Cloud storage for user avatars and chat images.          |
| **WebSockets** | **Socket.io**         | Bi-directional real-time communication.                  |

---

## 🚀 Getting Started

Follow these steps to set up the project locally.

### Prerequisites

- Node.js (v18+ recommended)
- npm or yarn
- A **MongoDB Atlas** account (or local MongoDB)
- A **Cloudinary** account

### Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/chatty-app.git
    cd chatty-app
    ```

2.  **Install dependencies:**

    For the entire project (root folders):

    ```bash
    # Install backend dependencies
    cd backend
    npm install

    # Install frontend dependencies
    cd ../frontend
    npm install
    ```

3.  **Configure Environment Variables:**
    Create a `.env` file in the `backend/` directory and add your credentials:

    ```env
    MONGODB_URI=your_mongodb_uri
    PORT=5001
    JWT_SECRET=your_jwt_secret
    CLOUDINARY_CLOUD_NAME=your_cloud_name
    CLOUDINARY_API_KEY=your_api_key
    CLOUDINARY_API_SECRET=your_api_secret
    NODE_ENV=development
    ```

4.  **Start the Development Servers:**

    **Backend:**

    ```bash
    cd backend
    npm run dev
    ```

    **Frontend:**

    ```bash
    cd frontend
    npm run dev
    ```

Visit `http://localhost:5173` to view the application.

---

## 🏗️ Architecture & Project Structure

The project follows a clean, decoupled client-server architecture:

### Backend (`/backend`)

- `src/controllers`: Request handlers for auth and messages.
- `src/models`: Mongoose schemas (User, Message).
- `src/routes`: Express API route definitions.
- `src/lib`: Core logic for DB connection, Socket.io setup, and Cloudinary.
- `src/middleware`: Custom auth and validation middleware.

### Frontend (`/frontend`)

- `src/components`: UI components (Navbar, ChatContainer, Sidebar, etc.).
- `src/pages`: Main view routes (Login, SignUp, Settings, Profile).
- `src/store`: Global state management using Zustand (auth, chat, theme).
- `src/lib`: Utility functions and Axios configuration.

---

## 📦 Building for Production

To create an optimized production build, the project is configured to serve the frontend from the backend:

1.  **Build the frontend:**

    ```bash
    cd frontend
    npm run build
    ```

2.  **Configure backend for production:**
    Ensure `NODE_ENV=production` is set in your environment variables.

3.  **Start the production server:**
    ```bash
    cd backend
    npm start
    ```

---

## 🎨 Credits

Designed and developed with ❤️ by **Fahad Asfaque**.

_Powered by MongoDB, Socket.io, and Cloudinary._

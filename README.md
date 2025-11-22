# LernCasino 🎰

A gamified learning application combining casino aesthetics with spaced repetition and level progression.

## Tech Stack
- **Frontend:** React, Vite, TailwindCSS
- **Backend:** Node.js, WebSocket (`ws`), MongoDB
- **Cloud:** Render (Backend) & Vercel (Frontend)

## 🚀 Setup & Local Development

1. **Install Dependencies**
   ```bash
   npm install
   ```

2. **Environment Variables**
   For local development, the app defaults to `localhost:8080` and a local file database if no variables are set.
   
   To connect to real cloud services locally, create a `.env` file:
   ```env
   MONGO_URI=mongodb+srv://... (Your MongoDB Atlas Connection String)
   VITE_WS_URL=ws://localhost:8080
   ```

3. **Start the App**
   You need two terminals:

   *Terminal 1 (Backend):*
   ```bash
   npm start
   ```
   
   *Terminal 2 (Frontend):*
   ```bash
   npm run dev
   ```

## ☁️ Deployment Guide

### 1. Backend (Render.com)
- **Build Command:** `npm install`
- **Start Command:** `node server.js`
- **Environment Variable:** `MONGO_URI` (Required for database persistence)

### 2. Frontend (Vercel.com)
- **Framework Preset:** Vite
- **Environment Variable:** `VITE_WS_URL`
  - Value: `wss://<DEIN-RENDER-NAME>.onrender.com` (Note: Use `wss://` for secure WebSockets)

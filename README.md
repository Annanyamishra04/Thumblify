# 🎨 Thumblify — AI Thumbnail Generator

Thumblify is a full-stack MERN application that lets users generate eye-catching,
click-worthy video thumbnails using AI — just by entering a title, choosing a
style, color scheme, and aspect ratio.



---

## ✨ Features

- 🔐 **User Authentication** — Secure signup & login with session-based auth
- 🖼️ **AI Thumbnail Generation** — Generate thumbnails from a title + prompt using AI
- 🎨 **Customization** — Choose aspect ratio (16:9, 1:1, 9:16), style (Bold & Graphic,
  Minimalist, Photorealistic, Illustrated, Tech/Futuristic), and color scheme
- 📂 **My Generations** — View, download, and delete all your generated thumbnails
- ☁️ **Cloud Storage** — Generated images are stored and served via Cloudinary
- 📱 **Responsive UI** — Smooth animations and a clean, modern interface

---

## 🛠️ Tech Stack

**Frontend**
- React (Vite + TypeScript)
- React Router DOM
- Tailwind CSS
- Motion (Framer Motion)
- Axios
- React Hot Toast

**Backend**
- Node.js + Express (TypeScript)
- MongoDB + Mongoose
- Express Session + Connect-Mongo
- bcrypt (password hashing)
- Cloudinary (image hosting)
- AI image generation API

---

## 📁 Project Structure

```
Thumblify/
├── backend/
│   ├── configs/        # DB, Cloudinary, AI client configs
│   ├── controllers/     # Route logic (Auth, Thumbnail, User)
│   ├── middleware/       # Auth protection middleware
│   ├── models/           # Mongoose schemas
│   ├── routes/            # Express routers
│   └── server.ts           # App entry point
│
└── frontend/
    ├── src/
    │   ├── components/   # Reusable UI components
    │   ├── pages/          # Route-level pages
    │   ├── sections/        # Landing page sections
    │   ├── context/          # Auth context
    │   ├── data/              # Static data (navlinks, styles, etc.)
    │   └── assets/             # Types & dummy data
    └── index.html
```

---

## ⚙️ Getting Started

### Prerequisites
- Node.js (v18+)
- MongoDB Atlas account (or local MongoDB)
- Cloudinary account
- An AI image generation API key

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/thumblify.git
cd thumblify
```

### 2. Setup the Backend
```bash
cd backend
npm install
```

Create a `.env` file inside `backend/`:
```env
PORT=3000
MONGODB_URI=your_mongodb_connection_string
SESSION_SECRET=your_session_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
GEMINI_API_KEY=your_gemini_api_key
FRONTEND_URL=http://localhost:5173
```

Run the backend:
```bash
npm run server
```

### 3. Setup the Frontend
```bash
cd ../frontend
npm install
```

Create a `.env` file inside `frontend/`:
```env
VITE_BASE_URL=http://localhost:3000
```

Run the frontend:
```bash
npm run dev
```

The app will be live at `http://localhost:5173` 🎉

---

## 🔑 API Endpoints

| Method | Endpoint                     | Description                  |
|--------|-------------------------------|-------------------------------|
| POST   | `/api/auth/register`          | Register a new user           |
| POST   | `/api/auth/login`              | Login user                     |
| GET    | `/api/auth/verify`              | Verify active session           |
| POST   | `/api/auth/logout`               | Logout user                      |
| POST   | `/api/thumbnail/generate`         | Generate a new thumbnail           |
| DELETE | `/api/thumbnail/delete/:id`        | Delete a thumbnail                  |
| GET    | `/api/user/thumbnails`              | Get all thumbnails for logged-in user |

---

## 🚀 Deployment

- **Frontend** — Deployed on Vercel
- **Backend** — Deployed on Vercel (Serverless Functions)
- **Database** — MongoDB Atlas

> Note: When deploying frontend and backend on different domains, make sure
> CORS `origin` and session cookie settings (`secure`, `sameSite`) are
> configured correctly to allow cross-site requests.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
Feel free to check the [issues page](#) if you want to contribute.

---

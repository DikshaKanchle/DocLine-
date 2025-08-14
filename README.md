# DocLine

This repository contains three separate apps managed together:

- **admin/** – Admin dashboard (Vite + Tailwind CSS)
- **frontend/** – Main client UI (Vite + Tailwind CSS)
- **backend/** – API server (Node.js + Express)

## 📂 Structure

```
Presrcipto-main/
  admin/       # Admin dashboard
  frontend/    # Client web app
  backend/     # API server
```

## 🚀 Setup Instructions

### 1. Clone and install dependencies

```bash
git clone <your-repo-url> presrcipto
cd presrcipto/Presrcipto-main
```

For each app (`admin`, `frontend`, `backend`), install dependencies:

```bash
cd admin
npm install

cd ../frontend
npm install

cd ../backend
npm install
```

### 2. Environment variables

Copy `.env.example` to each app and fill the values:

- **Admin (`admin/.env`)** – contains only `VITE_*` variables.
- **Frontend (`frontend/.env`)** – contains only `VITE_*` variables.
- **Backend (`backend/.env`)** – contains server-side variables (no `VITE_` prefix).

Example keys from `.env.example`:

```
ADMIN_EMAIL=
ADMIN_PASSWORD=
CLOUDINARY_API_KEY=
CLOUDINARY_NAME=
CLOUDINARY_SECRET_KEY=
JWT_SECRET=
MONGODB_URI=
PORT=
RAZORPAY_KEY_ID=
RAZORPAY_KEY_SECRET=
VITE_BACKEND_URL=
VITE_RAZORPAY_KEY_ID=
```

> **Tip:** Never commit your `.env` files. They are already listed in `.gitignore`.

### 3. Run locally

#### Admin
```bash
cd admin
npm run dev
```

#### Frontend
```bash
cd frontend
npm run dev
```

#### Backend
```bash
cd backend
npm run dev   # or npm start depending on scripts
```

### 4. Build for production

```bash
# Admin
cd admin
npm run build

# Frontend
cd ../frontend
npm run build

# Backend – usually no build step unless using TypeScript
```

### 5. GitHub upload

```bash
git init
git branch -M main
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

---

## 🛠 Tech Stack

- **Admin & Frontend:** Vite, React, Tailwind CSS, PostCSS
- **Backend:** Node.js, Express.js, MongoDB, JWT
- **Other:** Cloudinary, Razorpay

## 📄 License

MIT

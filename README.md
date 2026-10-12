# SOLESHIFT — Premium Sneaker Platform

[![React](https://img.shields.io/badge/Frontend-React%20%2B%20TypeScript-blue)](https://react.dev/)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI%20%2B%20Python-009688)](https://fastapi.tiangolo.com/)
[![Vite](https://img.shields.io/badge/Bundler-Vite-646CFF)](https://vitejs.dev/)
[![Database](https://img.shields.io/badge/Database-PostgreSQL%20%2F%20SQLite-336791)](https://www.postgresql.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**SOLESHIFT** is a modern, high-performance sneaker e-commerce and streetwear discovery platform. Built with a reactive **React + TypeScript** frontend powered by Vite and a robust **FastAPI** backend supporting authentication, cart & wishlist management, address profiles, and Razorpay checkout integration.

---

## 👟 Features

- **Sneaker Catalog & Filtering**: Browse premium collections, filter by size, brand, and category.
- **Shopping Cart & Wishlist**: Real-time sync, authenticated user cart persistence, and stock checks.
- **Seamless Checkout**: Address management, server-verified order creation, and Razorpay payment gateway integration.
- **Admin Dashboard**: Manage inventory, update sneaker stock, track shipments and incoming orders.
- **Secure Authentication**: Firebase token verification with backend role-based access control.

---

## 🛠️ Tech Stack

### Frontend
- **Framework**: React 18 / 19 with TypeScript
- **Tooling**: Vite, Oxlint
- **Deployment**: Firebase Hosting / Vercel

### Backend
- **Framework**: FastAPI (Python 3.12+)
- **ORM & Migrations**: SQLAlchemy 2.x & Alembic
- **Database**: PostgreSQL (Production) / SQLite (Local development)
- **Auth & Payments**: Firebase Admin SDK & Razorpay Python SDK

---

## 📂 Project Structure

```text
SOLESHIFT/
├── backend/                  # FastAPI backend application
│   ├── app/                  # Main application package
│   │   ├── api/routes/       # API endpoints (products, cart, payments, admin, etc.)
│   │   ├── core/             # Configuration & security auth
│   │   ├── db/               # Database connection and session management
│   │   ├── models/           # SQLAlchemy ORM models
│   │   ├── schemas/          # Pydantic request/response schemas
│   │   └── services/         # Order, payment, and product logic
│   ├── migrations/           # Alembic database migrations
│   ├── tests/                # Automated pytest suites
│   ├── requirements.txt      # Python dependencies
│   └── README.md             # Detailed backend documentation
├── public/                   # Static public assets
├── src/                      # React frontend application
│   ├── components/           # UI components
│   ├── pages/                # Application pages & routes
│   └── ...
├── .env.example              # Frontend environment variables template
├── index.html                # HTML entry point
├── package.json              # Frontend dependencies and scripts
└── vite.config.ts            # Vite build configuration
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18+) & npm
- Python (v3.11+) & pip

---

### 1. Frontend Setup

```bash
# Install dependencies
npm install

# Start Vite development server
npm run dev
```

The frontend will run at `http://localhost:5173`.

---

### 2. Backend Setup

```bash
# Navigate to backend directory
cd backend

# Create and activate virtual environment
python -m venv .venv

# Windows:
.venv\Scripts\activate
# macOS/Linux:
# source .venv/bin/activate

# Install backend dependencies
pip install -r requirements.txt

# Run migrations
alembic upgrade head

# Start FastAPI server
uvicorn app.main:app --reload --port 8000
```

The backend documentation will be available at:
- **Swagger UI**: `http://localhost:8000/docs`
- **ReDoc**: `http://localhost:8000/redoc`

---

## 🧪 Testing

### Backend Tests
```bash
cd backend
pytest
```

---

## 📄 License
This project is licensed under the MIT License.

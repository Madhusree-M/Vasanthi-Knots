# Vasanthi Knots - E-Commerce Fullstack Project

A full-stack e-commerce application built with React, Vite, Express, and MongoDB. This repository includes:

## Live Demo 
https://e-commerce-fe-ruddy.vercel.app/

- `e-commerce/` frontend (React + Vite)
- `express-ecommerce/` backend (Node.js + Express + MongoDB)

## 🧩 Features

### Frontend (`e-commerce/`)
- Product listing and search
- Product cards and detail flow
- Cart management + dynamic totals
- User authentication (sign-up, login)
- Checkout flow and order placement
- Admin area for product management
- Wishlist & profile pages
- Protected and private routes

### Backend (`express-ecommerce/`)
- REST API for products, cart, wishlist, orders
- Authentication with JWT
- CRUD endpoints for admin product management
- MongoDB models: User, Product, Cart, Wishlist, Order
- Middleware for authentication and protected routes

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm
- MongoDB (local or Atlas)

### 1. Setup backend

```bash
cd express-ecommerce
npm install
cp .env.example .env
# edit .env: MONGO_URI, JWT_SECRET, PORT (optional)
npm run dev
```

Backend default: `http://localhost:3000`

### 2. Setup frontend

```bash
cd ../e-commerce
npm install
cp .env.example .env
# edit .env: VITE_API_BASE_URL=http://localhost:3000 (or backend URL)
npm run dev
```

Frontend default: `http://localhost:5173`

## 🛠️ env vars

### Backend `.env` example

```
MONGO_URI=mongodb://localhost:27017/ecommerce
JWT_SECRET=supersecret
PORT=3000
```

### Frontend `.env` example

```
VITE_API_BASE_URL=http://localhost:3000/
```

## 📁 Project structure

- `e-commerce/src/components/`: React components (HomePage, Cart, Checkout, Auth, Admin, etc.)
- `e-commerce/src/layouts/`: UI layouts
- `express-ecommerce/routes/`: REST routes (`auth`, `cart`, `order`, `products`, `wishlist`)
- `express-ecommerce/controllers/`: controller logic
- `express-ecommerce/models/`: Mongoose models
- `express-ecommerce/middlewares/authMiddleware.js`: JWT auth middleware

## 🧪 Testing

No tests currently bundled. Add your preferred test runner (Jest, Vitest, etc.) in each folder.

## 🛡️ Notes

- Ensure CORS is enabled in backend for frontend origin.
- Use secure secrets in production (do not commit `.env`).

## 🚚 Deployment

- Backend: host on platforms like Render/Heroku/Vercel (serverless function for Express) or Railway.
- Frontend: host on Vercel/Netlify with `npm run build` and static site deployment.
- Set `VITE_API_BASE_URL` to production backend endpoint.

## 📌 Contribution

1. Fork repository
2. Create feature branch
3. Implement, test, lint
4. Create PR with description

---

Built for learning and quick e-commerce prototyping with modern React + Express stack.
# 🔄 Week 4: Deep Dive into MERN Stack Integration

## 🚀 Project Overview
A full-stack blog application built with the MERN stack demonstrating:
- RESTful API with Express & MongoDB Atlas
- JWT-based user authentication
- Full CRUD for blog posts and categories
- Comment system
- Responsive React frontend with Vite

## 🛠️ Setup Instructions

### Prerequisites
- Node.js v18+
- MongoDB Atlas account

### Installation
1. Clone the repository
2. **Backend**:
   ```bash
   cd server
   npm install
   cp .env.example .env  # Fill in MONGODB_URI and JWT_SECRET
   npm run dev


   3. Frontend:
       bash
      cd client
      npm install
      npm run dev

      Environment Variables (server/.env)
       env
      MONGODB_URI=mongodb+srv://user:pass@cluster.xxxx.mongodb.net/mern-stack
      JWT_SECRET=your_strong_random_secret_here
      PORT=5000 

📡 API Endpoints

Auth
POST /api/auth/register – { name, email, password }
POST /api/auth/login – { email, password }

Posts
GET /api/posts – Get all posts
GET /api/posts/:slug – Get single post
POST /api/posts – Create post (protected)
PUT /api/posts/:id – Update post (protected)
DELETE /api/posts/:id – Delete post (protected)
POST /api/posts/:postId/comments – Add comment (protected)

Categories
GET /api/categories
POST /api/categories (protected)


✅ Features Implemented
*Full MERN stack integration
*MongoDB Atlas with IP whitelist (0.0.0.0/0 for dev)
*JWT authentication with protected routes
*Full CRUD operations
*Comment system
*Custom React hooks (usePosts)
*Responsive UI with clean component architecture


🖼️ Screenshots

![Homepage](screenshots/home.png)
![Post Detail](screenshots/post-detail.png)


## 🌐 Live Deployment

- **Frontend (Vercel)**: [https://deployment-and-devops-essentials-eta.vercel.app](https://deployment-and-devops-essentials-eta.vercel.app)
- **Backend (Railway)**: [https://deployment-and-devops-essentials-jess-neemo-production.up.railway.app](https://deployment-and-devops-essentials-jess-neemo-production.up.railway.app)


## 🔧 DevOps Configuration

- **Frontend**: Vercel auto-deploys from `main` branch (`client/` root)
- **Backend**: Railway auto-deploys from `main` branch (`server/` root)
- **Environment**: All secrets managed via platform environment variables
- **Database**: MongoDB Atlas with `0.0.0.0/0` IP whitelist (per [Atlas Security Docs](https://www.mongodb.com/docs/atlas/security-whitelist/)) for Railway compatibility
- **CI/CD**: Fully automated — push to GitHub → auto-build and deploy
# Deployment Guide for Fullstack Chat App

## Prerequisites
- GitHub repository: ✅ Done
- MongoDB Atlas account (free)
- Railway/Render account (free)
- Vercel account (free)

## Step 1: Setup MongoDB Atlas (Cloud Database)
1. Go to [MongoDB Atlas](https://www.mongodb.com/atlas)
2. Create free account
3. Create new cluster (M0 free tier)
4. Create database user
5. Get connection string

## Step 2: Deploy Backend (API Server)
### Option A: Railway (Recommended)
1. Go to [Railway.app](https://railway.app)
2. Connect GitHub account
3. Deploy from GitHub repo
4. Select backend folder
5. Add environment variables

### Option B: Render
1. Go to [Render.com](https://render.com)
2. Connect GitHub account
3. Create new Web Service
4. Connect your repository

## Step 3: Deploy Frontend
1. Go to [Vercel.com](https://vercel.com)
2. Connect GitHub account
3. Import your repository
4. Set build settings for frontend folder
5. Add environment variable for backend URL

## Step 4: Update Configuration
- Update CORS settings in backend
- Update API base URL in frontend
- Configure environment variables

## Environment Variables Needed:
### Backend:
- PORT=5001
- NODE_ENV=production
- MONGODB_URI=<your-atlas-connection-string>
- JWT_SECRET=<your-secret>
- CLOUDINARY_CLOUD_NAME=<optional>
- CLOUDINARY_API_KEY=<optional>
- CLOUDINARY_API_SECRET=<optional>

### Frontend:
- VITE_API_URL=<your-backend-url>
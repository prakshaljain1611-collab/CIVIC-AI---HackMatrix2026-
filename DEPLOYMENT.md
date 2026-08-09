# 🚢 Production Deployment Guide — CivicAI

## ☁️ Option 1: Vercel Deployment (Recommended)
1. Push repository to GitHub.
2. Import project into Vercel dashboard.
3. Configure environment variables (`AI_API_KEY`, `SESSION_SECRET`, `DATABASE_URL`).
4. Vercel automatically detects `vercel.json` and routes `/api/*` to `backend/api/index.ts`.

## 🐳 Option 2: Docker Container Deployment
```bash
# Build and run containers with Docker Compose
docker-compose -f docker/docker-compose.yml up --build -d
```

## 🖥️ Option 3: Manual Node.js VPS / Cloud Run
```bash
# Build production assets
npm run build

# Start backend server
PORT=8787 NODE_ENV=production node backend/index.ts
```

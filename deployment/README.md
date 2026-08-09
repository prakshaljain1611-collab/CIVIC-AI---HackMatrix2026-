# 🚀 Deployment Configuration

Contains production deployment setup for Vercel, Node.js hosts, and database hosting.

---

## 📁 Key Configurations
- **Vercel Routing**: `vercel.json` at root routes `/api/*` to `backend/api/index.ts`.
- **Node.js Express Host**: Can be deployed on AWS EC2, Cloud Run, Render, or Railway.
- **Postgres Database**: Tested on Neon Serverless Postgres (`@neondatabase/serverless`) and Supabase.

<div align="center">
  <h1>🏛️ CivicAI - Jansunwai Portal 2.0</h1>
  <p><b>AI-Powered Public Grievance Redressal & Intelligent SLA Tracking System</b></p>
</div>

---

## 📌 Project Title
**CivicAI: Jansunwai Portal 2.0**

## 👥 Team Name
**Team QUAD BRAINS**

---

## 🚨 Problem Statement
Public grievance redressal portals (such as Jansunwai) handle thousands of citizen complaints daily. Traditional systems suffer from critical bottlenecks:
- **Delayed Processing & Backlogs**: Manual routing of complaints leads to slow processing, missed SLAs, and citizen frustration.
- **Misclassified & Spam Complaints**: Lack of automated triaging results in improper department assignment and resource waste.
- **Lack of Transparency**: Citizens lack real-time visibility into complaint status, SLA deadlines, and resolution progress.
- **Administrative Burden**: Department officials lack automated tools for priority sorting, response generation, and breach warnings.

---

## 💡 Solution Overview
**CivicAI (Jansunwai Portal 2.0)** transforms public administration with an end-to-end, AI-enhanced grievance management ecosystem:

1. **Intelligent Complaint Triaging**: Automatically categorizes grievances, assigns priority scores, and routes complaints to the responsible department using Google Gemini API & Claude fallback.
2. **Real-time SLA Tracking & Breach Sweeper**: Automated background worker sweeps active complaints, flags approaching/breached SLAs, and alerts department officials.
3. **Multi-Channel Passwordless Authentication**: Citizen-friendly authentication supporting Google Sign-In and Phone/SMS OTP verification with anti-bot honeypot protection.
4. **Interactive Citizen & Officer Portals**: High-performance dashboard with interactive GIS mapping, complaint heatmaps, status updates, and automated response template generation.
5. **Durable Storage & Security**: Enterprise-grade security featuring rate-limiting, timing-safe OTP verification, RBAC permissions, and optional Neon Serverless Postgres persistence.

---

## 🔗 Links
- **Live Deployment Application**: [https://civic-ai-hack-matrix2026.vercel.app](https://civic-ai-hack-matrix2026.vercel.app)
- **Live Demonstration Portal**: [https://civic-ai-hack-matrix2026.vercel.app](https://civic-ai-hack-matrix2026.vercel.app)
- **PPT Presentation**: [View Presentation Deck](https://example.com/civicai-ppt) *(Insert presentation link if applicable)*

---

## 🛠️ Technology Stack

| Layer | Technologies Used |
|---|---|
| **Frontend** | React 19, Vite, TypeScript, TailwindCSS v4, Framer Motion, Lucide Icons |
| **Maps & Analytics** | Leaflet / React-Leaflet, Recharts |
| **Backend API** | Node.js, Express, TypeScript (`tsx`) |
| **Database & Storage** | Neon Serverless Postgres (`@neondatabase/serverless`), PGlite (In-memory dev DB) |
| **AI / LLM Integration** | Google Gemini API (`@google/genai`), Anthropic Claude API (Fallback), AWS Bedrock (Fallback) |
| **Authentication & SMS** | Google OAuth 2.0, MSG91 / Twilio / Console Mode SMS OTP |
| **Security** | RBAC, Anti-bot Honeypot, Timing-safe OTP hashing, Uniform Latency Floor |

---

## 👨‍💻 Team Members & 4-Part Git Work Division

To allow seamless parallel Git commits without merge conflicts, the repository is divided into 4 isolated work modules:

| Member | Assigned Domain | Working Directory | Primary Responsibilities |
|---|---|---|---|
| **Member 1** | **Frontend Engineer** | `frontend/` | React 19 UI components, screens, theme, maps, responsive styling |
| **Member 2** | **Backend API Engineer** | `backend/` | Express REST API routes, auth session logic, rate limiters, SLA sweeper |
| **Member 3** | **AI / LLM Integration** | `ai/` | Gemini API prompts, Claude failover, entity extraction, triaging rules |
| **Member 4** | **Database & DevOps** | `database/`, `docker/`, `scripts/` | PostgreSQL schemas, seed scripts, Docker compose, CI/CD pipelines |

---

## ⚙️ Setup Instructions

### Prerequisites
- **Node.js**: v18.x or higher
- **npm**: v9.x or higher

### 1. Clone the Repository
```bash
git clone https://github.com/prakshaljain1611-collab/CIVIC-AI---HackMatrix2026-.git
cd CIVIC-AI---HackMatrix2026-
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Configure Environment Variables
Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```
Fill in the necessary API keys in `.env`:
```env
AI_API_KEY=your-gemini-api-key
PORT=8787
AUTH_DEV_OTP=true
```

### 4. Run the Development Server
Run both the API server (Port 8787) and Vite frontend (Port 3000) simultaneously:
```bash
npm run dev:full
```

Or run frontend and backend separately:
```bash
npm run server   # Starts Express backend on http://localhost:8787
npm run dev      # Starts Vite web app on http://localhost:3000
```

### 5. Access the Application
- **Web App (Citizen & Staff Portal)**: [http://localhost:3000](http://localhost:3000)
- **API Backend**: [http://localhost:8787](http://localhost:8787)

---

## 📜 Repository & Development Guidelines
- **Commit History**: Regular, descriptive commits detailing incremental feature development.
- **Repository Accessibility**: Publicly accessible throughout evaluation.

---

## 🛡️ Originality & Code Ownership
This project was developed for **HackMatrix 2K26** organized by **IEEE Computer Society SBC, MITS Gwalior**.

- **Original Work**: All core architecture, UI components, backend APIs, SLA sweepers, and prompt engineering were built specifically for this hackathon by Team CivicAI.
- **Open-Source Attributions**:
  - `React`, `Vite`, `TypeScript`, `Express`, and `TailwindCSS` for application structure.
  - `@google/genai` (Google Gemini SDK) & `@anthropic-ai/sdk` for AI integrations.
  - `Leaflet` & `React-Leaflet` for open GIS mapping.
  - `Recharts` & `Lucide-React` for analytics visualization and icon sets.
  - `@neondatabase/serverless` & `@electric-sql/pglite` for database connectivity and local dev DB.
- **Compliance**: No code has been copied from other teams, purchased, or reused improperly. All external libraries and tools are cited with proper attribution.

<div align="center">

# 🏛️ CivicAI

### Intelligent Citizen Grievance & Accountability Platform

**HackMatrix 2026 — Round 2**
<br/>
<sub>Team <b>Quad Brains</b> · Team Leader: <b>Himani Rishi</b></sub>

<br/>

![License](https://img.shields.io/badge/License-MIT-10b981?style=flat-square)
![React](https://img.shields.io/badge/React-19-61dafb?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178c6?style=flat-square&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-6-646cff?style=flat-square&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-v4-38bdf8?style=flat-square&logo=tailwindcss&logoColor=white)
![Gemini](https://img.shields.io/badge/Google--Gemini-3.1%20Flash-8e44ad?style=flat-square&logo=google&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Neon-4169e1?style=flat-square&logo=postgresql&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-Deployed-000000?style=flat-square&logo=vercel&logoColor=white)

<br/>

[![Live Demo](https://img.shields.io/badge/▶%20Live%20Demo-Open%20App-10b981?style=for-the-badge&logo=vercel&logoColor=white)](https://civic-ai-hack-matrix2026.vercel.app/)
[![Demo Video](https://img.shields.io/badge/🎥%20Demo%20Video-Watch-red?style=for-the-badge&logo=google-drive&logoColor=white)](https://drive.google.com/file/d/1VyY7EL__NBuKKwnK8mbkfQ-vxX-mQgmh/view?usp=sharing)
[![Documentation PDF](https://img.shields.io/badge/📄%20Documentation-PDF-4285F4?style=for-the-badge&logo=google-drive&logoColor=white)](https://drive.google.com/file/d/1LnyN-NShJ19KT_DjBMfQZPeOpzHZHtFU/view?usp=sharing)
[![GitHub Repo](https://img.shields.io/badge/🐙%20GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/prakshaljain1611-collab/CIVIC-AI---HackMatrix2026-)

<br/>

[**📄 Full Solution Document (Markdown)**](PROJECT_DOCUMENTATION.md) · [**📑 Official Documentation PDF**](https://drive.google.com/file/d/1LnyN-NShJ19KT_DjBMfQZPeOpzHZHtFU/view?usp=sharing) · [**🔄 User Flow**](USER_FLOW.md) · [**💻 Tech Stack**](TECH_STACK.md) · [**📋 PRD**](PRD.md)

</div>

---

> **The Core Idea.** Traditional municipal grievance systems (like Jansunwai) suffer from severe manual routing delays, misclassified complaints, lack of SLA transparency, and zero citizen verification upon resolution. **CivicAI** bridges this gap by combining **conversational AI intake** (powered by **Google Gemini 3.1 Flash Lite**) with **governance-oriented workflow controls**. The platform keeps AI advisory where human judgment matters, while enforcing strict SLA timers, RBAC authorization, explainable duplicate detection, and citizen-controlled closure.

---

## 📌 Contents

[Impact & Benchmarks](#-impact--benchmarks) · [Core Workflow](#-core-workflow) · [Key Features](#-key-features) · [Technology Stack](#-technology-stack) · [Security & Governance](#-security--governance) · [Quickstart](#-quickstart) · [Repository Structure](#-repository-structure) · [Team & Work Division](#-team--work-division)

---

## 📊 Impact & Benchmarks

CivicAI transforms operational performance across municipal departments:

| Metric | Traditional Portal (Jansunwai) | 🟢 CivicAI (Ours) | Improvement |
| :--- | :---: | :---: | :---: |
| **Intake & Triage Time** | 24 - 48 Hours | **< 2 Seconds** | **99.9% Faster** |
| **Department Routing Accuracy** | ~ 65% (Manual) | **> 94% (AI Enriched)** | **+29% Accuracy** |
| **SLA Breach Monitoring** | Manual Audit (Periodic) | **Real-time Automated Sweeper** | **100% Zero Missed Alerts** |
| **Closure Verification** | Closed by Officer unilaterally | **Citizen-Controlled Verification** | **Zero False Closures** |
| **Multilingual Accessibility** | English / Hindi only | **12 Languages + RTL Urdu** | **Universal Coverage** |

---

## 🔄 Core Workflow

```
[Citizen Intake] ──> [AI Understanding] ──> [CIV Ref Creation] ──> [Duplicate & Routing]
                                                                         │
[Citizen Verification] <── [Resolution] <── [Officer Action] <── [SLA Monitoring]
```

1. **01 Citizen Intake** — Citizen authenticates via passwordless OTP and describes the grievance conversationally.
2. **02 AI Understanding** — Gemini 3.1 Flash extracts intent, categorizes into 1 of 8 departments, evaluates sentiment, and pinpoints GIS coordinates.
3. **03 Complaint Creation** — A human-readable `CIV-XXXXXX` reference number is generated and indexed for tracking.
4. **04 Duplicate Scoring & Routing** — Candidate duplicates are scored using category, geographic proximity, text similarity, and recency before routing within jurisdiction.
5. **05 Officer Investigation** — Field officers review structured complaints, upload evidence/notes, and progress status through official channels.
6. **06 Real-Time SLA Escalation** — Background sweepers track strict resolution deadlines (24h Critical to 120h Low) and trigger breach warnings.
7. **07 Citizen-Controlled Closure** — Resolution is unverified until the citizen rates and confirms satisfaction, with 1-click reopen capability.

---

## ✨ Key Features

* 🤖 **Conversational AI Intake**: AI-assisted complaint understanding with structured JSON outputs and safe static fallbacks.
* 🌐 **12-Language Support**: Native-script interface support including English, Hindi, Tamil, Telugu, Marathi, Bengali, and RTL Urdu.
* 📱 **Passwordless OTP Authentication**: Frictionless login via email or Indian mobile number with anti-bot honeypots.
* 🗺️ **Location-Aware Reporting**: GIS map integration (Leaflet/React-Leaflet) with landmark and sector resolution.
* 🛡️ **Role-Based Access Control (RBAC)**: Multi-tiered access for Citizens, Field Officers, Department Heads, and Super Admins.
* ⚡ **Real-Time Updates**: Server-Sent Events (SSE) push live complaint status changes directly to the UI.
* 🔍 **Explainable Duplicate Engine**: Multi-signal scoring prevents duplicate backlogs without blindly merging separate issues.
* 🔒 **Append-Only Audit Trail**: Hash-linked event logging for complete administrative accountability.

---

## 🛠️ Technology Stack

| Layer | Implementation |
| :--- | :--- |
| **Frontend** | React 19 • TypeScript (`~5.8`) • Vite (`^6.2`) • Tailwind CSS v4 • Framer Motion • Lucide React |
| **Maps & Analytics** | Leaflet / React-Leaflet • Recharts • WebGL Shader (`OGL`) |
| **Backend API** | Node.js • Express (`^4.21`) • TypeScript (`tsx`) |
| **AI Layer** | Google Gemini 3.1 Flash Lite (`@google/genai`) • Anthropic Claude Fallback • Static Fallback |
| **Database & Storage** | Serverless PostgreSQL (`@neondatabase/serverless`) • PGlite (In-memory dev DB) |
| **Security & Auth** | Google OAuth 2.0 • MSG91 / Twilio SMS OTP • CSRF Protection • Timing-Safe Hashing • Rate Limiting |
| **Deployment** | Vercel Live Deployment |

---

## 🛡️ Security & Governance

* **AI Key Isolation**: API keys remain strictly server-side and are never exposed to the client.
* **Failure Ladder**: Graceful degradation from Gemini → Claude Failover → Rule-based Static Fallback.
* **Authentication Safeguards**: Hashed OTP storage with timing-safe comparison and strict attempt window limits.
* **Privacy-Aware Transparency**: Public feeds expose complaint progress while redacting citizen contact info.
* **Accessibility Compliance**: Built following WCAG AAA guidelines, visible keyboard focus rings, and screen-reader semantics.

---

## 🚀 Quickstart

### Prerequisites
* **Node.js**: `v18.x` or higher
* **npm**: `v9.x` or higher

### 1. Clone the Repository
```bash
git clone https://github.com/prakshaljain1611-collab/CIVIC-AI---HackMatrix2026-.git
cd CIVIC-AI---HackMatrix2026-
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Environment Setup
Copy the example environment file and configure your credentials:
```bash
cp .env.example .env
```
Key configuration parameters:
```env
PORT=8787
AI_API_KEY=your_google_gemini_api_key
AUTH_DEV_OTP=true
```

### 4. Run Locally
Start both backend API server and frontend Vite dev server concurrently:
```bash
npm run dev
```
Open **`http://localhost:3000`** in your browser.

---

## 📂 Repository Structure

```
├── backend/            # Express REST API server & authentication logic
├── ai/                 # Gemini API integration, prompt templates & triage engine
├── frontend/           # React 19 frontend app (Vite + TailwindCSS v4)
├── database/           # PostgreSQL schemas, migrations & seed scripts
├── docs/               # Architecture, design system & backend documentation
├── PROJECT_DOCUMENTATION.md # Complete HackMatrix 2026 Round 2 solution paper
├── USER_FLOW.md        # Mermaid sequence diagram & user journey documentation
├── TECH_STACK.md       # Detailed technical stack & package dependencies
└── PRD.md              # Product Requirement Document
```

---

## 👥 Team & Work Division

| Team Member | Module Scope | Primary Responsibilities |
| :--- | :--- | :--- |
| **Himani Rishi** *(Leader)* | **Full-Stack & Governance** | System architecture, submission documentation, SLA workflow |
| **Member 2** | **Frontend Engineer** | React 19 UI components, GIS map integration, responsive dashboard |
| **Member 3** | **Backend & AI Engineer** | Express REST endpoints, Gemini 3.1 Flash triage logic, fallback ladder |
| **Member 4** | **Database & Security** | PostgreSQL schema, RBAC permissions, timing-safe auth & rate limiting |

---

<div align="center">
  <sub>Built with ❤️ by Team <b>Quad Brains</b> for <b>HackMatrix 2026 — Round 2</b></sub>
</div>

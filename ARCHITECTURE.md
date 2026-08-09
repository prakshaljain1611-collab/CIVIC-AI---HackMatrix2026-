# 🏗️ Architecture Specification — CivicAI

## 1. High-Level Architecture Overview
CivicAI follows a clean, decoupled 4-tier architecture:

```
[ Citizen & Officer Clients ]
           │ (HTTP / SSE)
           ▼
[ Vite / Express API Server (:8787) ]
  ├── Auth & Session Guard (Express Cookie + Bearer)
  ├── Rate Limiters (Fixed Window Memory Store)
  ├── AI Triaging Engine (Gemini 3.1 Flash + Claude Fallback)
  ├── SLA Sweep Engine (Cron-like 5-min intervals)
  └── Store Layer (PostgreSQL / In-Memory PGlite)
```

## 2. Frontend Architecture
- **Framework**: React 19 + TypeScript + Vite.
- **Routing**: `react-router-dom` v7 with lazy-loaded admin bundle boundary (`/portal/admin`).
- **Styling**: Vanilla CSS tokens in `src/index.css` + TailwindCSS v4.
- **State Management**: React Context (`AuthContext`, `ThemeContext`, `I18nContext`).
- **Visuals & Motion**: Framer Motion, Lucide React icons, WebGL background effects via `ogl`.

## 3. Backend Architecture
- **Framework**: Express.js in ESM mode run via `tsx watch`.
- **Security**: Security headers (Helmet-like custom headers), rate limiting, timing-safe crypto comparison, bot honeypots.
- **Resilience**: Concurrency limiters (max 4 concurrent AI requests), body size caps (64KB), daily global API caps.

## 4. AI & Provider Failover Architecture
```
User Complaint
      │
      ▼
Google Gemini API (Primary) ──► Fail? ──► AWS Bedrock (Claude Haiku) ──► Fail? ──► Anthropic Claude Direct ──► Static Fallback
```

## 5. Security & Isolation Boundaries
- Web app and Admin portal are isolated route trees so admin code never ships to citizen bundles.
- Passwordless OTP auth uses timing-safe hash comparison (`crypto.timingSafeEqual`) and SHA-256 code hashing.

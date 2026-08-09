# 📊 Pitch Deck Content (HackMatrix 2K26) — CivicAI

---

## Slide 1: Title & Team
- **Title**: CivicAI — Jansunwai Portal 2.0
- **Subtitle**: AI-Powered Public Grievance Redressal & SLA Enforcement System
- **Live Demo Link**: [https://civic-ai-hack-matrix2026.vercel.app](https://civic-ai-hack-matrix2026.vercel.app)
- **Team Name**: Team CivicAI
- **Event**: HackMatrix 2K26 (IEEE Computer Society SBC, MITS Gwalior)

---

## Slide 2: The Problem
- **Manual Bottlenecks**: 10,000+ daily grievances processed manually.
- **SLA Violations**: Over 35% of citizen grievances exceed resolution deadlines.
- **Opacity**: Zero real-time tracking for citizens; high frustration.

---

## Slide 3: The Solution — CivicAI
- **Instant AI Triaging**: Categorizes into 8 departments, scores priority, and extracts location in < 2 seconds.
- **Real-Time SLA Sweeper**: Automated background worker sweeps active grievances every 5 minutes and flags impending breaches.
- **Passwordless Security**: Google One-Tap + Phone/SMS OTP login with timing-safe SHA-256 code hashing.

---

## Slide 4: System Architecture & Failover
- **Frontend**: React 19, Vite, TailwindCSS v4, Leaflet GIS Maps.
- **Backend**: Express API, Neon Serverless Postgres, Server-Sent Events.
- **AI Failover Ladder**: Gemini 3.1 Flash → AWS Bedrock → Anthropic Claude → Static Fallback.

---

## Slide 5: Impact & Demonstration
- 90% reduction in complaint routing latency.
- 100% SLA breach detection transparency.
- WCAG AAA accessible design.

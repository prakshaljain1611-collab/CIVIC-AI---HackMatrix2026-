# 🏛️ PROJECT DOCUMENTATION | HACKMATRIX 2026 – ROUND 2

## CivicAI — Intelligent Citizen Grievance & Accountability Platform

| Attribute | Details |
|---|---|
| **TEAM** | Quad Brains |
| **TEAM LEADER** | Himani Rishi |
| **PROJECT** | CivicAI |
| **EVENT** | HackMatrix 2026 – Round 2 |

> **Tagline**: AI-assisted intake • Smart routing • SLA escalation • Transparency • Citizen verification

---

## 🔗 Official References & Submission Links
- **GitHub Repository**: [https://github.com/prakshaljain1611-collab/CIVIC-AI---HackMatrix2026-](https://github.com/prakshaljain1611-collab/CIVIC-AI---HackMatrix2026-)
- **Live Deployment**: [https://civic-ai-hack-matrix2026.vercel.app/](https://civic-ai-hack-matrix2026.vercel.app/)
- **Demo Video**: [https://drive.google.com/file/d/1VvY7EL__NBuKKwnK8mbkfQ-vxX-mQgmh/view?usp=sharing](https://drive.google.com/file/d/1VvY7EL__NBuKKwnK8mbkfQ-vxX-mQgmh/view?usp=sharing)
- **Official Documentation PDF**: [https://drive.google.com/file/d/1LnyN-NShJ19KT_DjBMfQZPeOpzHZHtFU/view?usp=sharing](https://drive.google.com/file/d/1LnyN-NShJ19KT_DjBMfQZPeOpzHZHtFU/view?usp=sharing)

---

## 🚨 The Challenge

### Problem Statement
Citizens often face friction when reporting civic issues: they may not know the correct department, complaints can be difficult to track after submission, duplicate reports can overload staff, and delayed cases can remain unresolved without clear accountability. CivicAI addresses this gap by providing a single, AI-assisted entry point for reporting, classifying, routing, tracking and resolving civic grievances.

---

## 💡 What CivicAI Delivers

### Project Overview
CivicAI is a full-stack civic grievance platform that connects a citizen-facing conversational interface with an administrative resolution workflow. AI helps structure an unstructured complaint into useful fields such as category, priority, sentiment and location, while the platform maintains a controlled lifecycle from submission through department assignment, investigation, resolution, citizen verification and closure.

---

## 🔄 Core Journey — End-to-End Workflow

1. **01 Citizen Intake** — Citizen signs in using passwordless OTP and describes the issue conversationally.
2. **02 AI Understanding** — The system extracts intent, category, priority, sentiment and location; it can ask for missing details.
3. **03 Complaint Creation** — A human-readable complaint reference is generated and the issue becomes trackable.
4. **04 Duplicate & Routing** — Potential duplicates are scored using category, geography, text overlap and recency; the complaint is routed within jurisdiction.
5. **05 Officer Action** — Authorized officers investigate, update status, add notes/evidence and progress the complaint through the workflow.
6. **06 SLA & Escalation** — Open complaints are monitored against deadlines; missed targets increase escalation level and generate events.
7. **07 Citizen Verification** — A resolved complaint can be verified by the citizen, rated, closed or reopened when the issue is not actually resolved.

---

## ⭐️ Why CivicAI Stands Out

### USP — Unique Selling Proposition
CivicAI is not positioned as a chatbot layered on top of a complaint form. Its differentiator is the combination of AI-assisted understanding with governance-oriented workflow controls. The platform keeps automation advisory where uncertainty matters, while enforcing authorization, jurisdiction, SLA and closure rules at the application/backend level.

* **Explainable duplicate detection** — Potential duplicates are identified through multiple signals instead of blindly merging complaints.
* **Accountability by design** — SLA deadlines, escalation levels, status history and audit records make progress traceable.
* **Citizen-controlled closure** — Resolution is not treated as complete until the citizen can verify the outcome.
* **Privacy-aware transparency** — Public complaint information can be exposed without publishing citizen contact details.
* **Production-minded security** — Rate limits, CSRF/session protections, RBAC, input limits and server-side scope checks are built into the platform.
* **Accessible civic UX** — The design system targets WCAG AAA practices, keyboard access, screen-reader semantics and reduced motion.

---

## 🛠️ Feature Set

### Key Features
* **Conversational AI Intake** — AI-assisted complaint understanding with structured outputs and safe fallback behavior.
* **12-Language Interface** — CivicAI ships with twelve language options and native-script support, including RTL handling for Urdu.
* **Passwordless OTP Authentication** — Citizens can authenticate through email or Indian mobile number without requiring Aadhaar.
* **Smart Complaint Filing** — Each complaint receives a human-friendly CIV reference number for tracking.
* **Location-Aware Reporting** — Landmarks, sector patterns and browser GPS can contribute to location resolution.
* **AI Priority & Classification** — Complaints can be classified and prioritized to support faster operational handling.
* **Duplicate Detection** — Candidate duplicates are scored using category, geographic proximity, text similarity and recency.
* **Role-Based Access Control** — Administrative roles are separated and constrained by state, district, department and officer scope.
* **SLA Monitoring & Escalation** — Open complaints carry deadlines and escalation levels, supporting accountability for overdue cases.
* **Controlled Resolution Workflow** — Submitted → AI Verification → Assignment → Investigation/Field Visit → Work → Resolved → Citizen Verification → Closed.
* **Evidence & Media** — Complaint media is validated before being accepted and stored by reference rather than as database blobs.
* **Live Updates** — Server-sent events support live complaint/event updates in the interface.
* **Transparency Feed** — Public views can expose civic issue progress while filtering sensitive citizen information.
* **Audit Trail** — Audit records are designed as append-only, hash-linked records to make historical changes detectable.
* **Admin Analytics** — Administrative views support overview, workload and operational analytics.

---

## 💻 Engineering

### Technology Stack

| Layer | Implementation |
|---|---|
| **Frontend** | React 19 • TypeScript • Vite • Tailwind CSS • React Router • React Leaflet • Recharts • Lucide React • Motion/Framer Motion |
| **Backend** | Node.js • Express • TypeScript/tsx |
| **AI Layer** | Google Gemini through the Google GenAI SDK, with optional Claude failover and static fallback behavior |
| **Database** | PostgreSQL/Neon with SQL schema, indexes, constraints and row-level security policies |
| **Maps & Location** | Leaflet / React-Leaflet • browser geolocation • landmark/sector resolution |
| **Realtime** | Server-Sent Events for live updates |
| **Security** | OTP hashing • timing-safe comparison • session controls • rate limiting • CSRF protection • request/body limits • RBAC |
| **Deployment** | Vercel live deployment |

---

## 🛡️ Built for Civic Use

### Security, Reliability & Responsible AI
* **AI key isolation** — AI provider keys remain on the backend rather than being exposed to the browser.
* **Usage protection** — AI input, history, output, concurrency and daily budgets are bounded to reduce abuse and runaway usage.
* **Failure ladder** — The AI layer can move from Gemini to optional Claude failover and then a static fallback, allowing the application to degrade gracefully.
* **Authentication safeguards** — OTP codes are hashed, compared using timing-safe comparison, expire after a defined window and are protected by attempt/request limits.
* **Server-side authorization** — Administrative scope checks are enforced beyond the UI, reducing reliance on client-side hiding.
* **Data integrity** — Database constraints cover key invariants such as valid coordinates, non-self duplicates and closed complaints having a close date.

---

## 🗄️ Persistence

### Database & Data Model
The database schema separates users, roles, departments, officers, complaints, complaint media and complaint status history, while supporting jurisdiction-aware indexing and SLA-focused queries. Complaint records store AI-derived fields alongside human-entered information, allowing the administrative workflow to use automation without losing the original complaint context.

---

## 🎨 Public-Sector UX

### Accessibility & Design
The project design system explicitly targets accessible and ethical government/public-sector UX. It uses Lexend for headings and Source Sans 3 for body text, maintains high-contrast color tokens, provides visible keyboard focus states, minimum touch targets, semantic form feedback and reduced-motion behavior. Functional icons use SVG iconography rather than emoji.

---

## 📈 Expected Value

### Impact
* **For citizens** — A simpler way to report problems, understand status, receive updates and verify resolution.
* **For officers** — Structured complaints, clearer prioritization, jurisdiction-aware work queues and operational context.
* **For administrators** — SLA visibility, escalation, workload analytics, transparency and auditability.
* **For governance** — A traceable digital workflow that can turn fragmented grievance handling into measurable service delivery.

---

## 🚀 Scale Beyond the Prototype

### Future Scope
Future iterations can strengthen production readiness through Redis-backed distributed session/rate-limit state, scheduled background SLA sweeps, object storage at scale, richer GIS/geocoding, voice-first complaint filing, OCR for supporting documents, predictive civic hotspot analytics, department-specific AI models, official notification/identity integrations and dedicated mobile applications.

---

## 🎬 Recommended 3-Minute Narrative

### Hackathon Demo Story
1. **Report** — Show a citizen describing a real civic issue in the conversational interface.
2. **Understand** — Show AI extracting category/priority/location and producing a structured complaint.
3. **Track** — Show the generated CIV reference and complaint status.
4. **Operate** — Switch to the admin portal and demonstrate scoped complaint handling and assignment.
5. **Escalate** — Show SLA/escalation visibility for an overdue case.
6. **Verify** — Return to the citizen view and demonstrate resolution verification/reopen behavior.

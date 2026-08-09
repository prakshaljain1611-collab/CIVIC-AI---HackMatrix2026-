# 📁 File & Directory Structure — CivicAI

```
CIVI-AI-PRJ/
├── README.md                 # Master project documentation
├── PRD.md                    # Product Requirement Document
├── ARCHITECTURE.md           # System & security architecture
├── TECH_STACK.md             # Stack overview & dependencies
├── DATABASE.md               # PostgreSQL schema & tables
├── API.md                    # REST API endpoints & schemas
├── FEATURES.md               # Citizen & admin features
├── USER_FLOW.md              # User interaction & sequence diagrams
├── UI_GUIDELINES.md          # Design system & WCAG guidelines
├── CODING_RULES.md           # Engineering guidelines
├── FILE_STRUCTURE.md         # Repository map (this file)
├── TASKS.md                  # Task roadmap & team assignments
├── PROMPTS.md                # System prompts for AI triaging
├── CHANGELOG.md              # Version milestones
├── ROADMAP.md                # Future feature roadmap
├── ENVIRONMENT.md            # Environment variable specification
├── SECURITY.md               # Security boundaries & guards
├── TESTING.md                # Testing strategy & commands
├── DEPLOYMENT.md             # Docker & production setup
├── DEMO_SCRIPT.md            # Live presentation script
├── PPT_CONTENT.md            # Hackathon pitch deck slides
├── FAQ.md                    # Frequently asked questions
├── LICENSE.md                # Project license terms
│
├── frontend/                 # Member 1 Domain: React 19 Frontend
│   └── src/                  # App, Components, Hooks, Context, i18n
├── backend/                  # Member 2 Domain: Express API Backend
│   ├── index.ts              # API entrypoint
│   └── api/                  # Vercel serverless entry
├── ai/                       # Member 3 Domain: AI Models & Prompts
├── database/                 # Member 4 Domain: Database Schemas & Seeds
│   ├── 001_schema.sql        # Database schema
│   ├── 002_rls.sql           # Row level security
│   └── seed.mjs              # Seed data script
├── admin/                    # Admin portal specs & documentation
├── shared/                   # Shared types & contracts
├── mobile/                   # Mobile / PWA setup
├── scripts/                  # Dev scripts (dev.mjs, doctor.mjs)
├── .github/                  # CI/CD workflows
├── docker/                   # Dockerfile & Compose configs
├── deployment/               # Vercel & cloud deployment
├── diagrams/                 # Mermaid architecture diagrams
├── docs/                     # Detailed technical docs
├── assets/                   # Brand logos and design tools
└── research/                 # Historical prototypes & research
```

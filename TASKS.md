# 📋 Tasks & Team Work Division — CivicAI

## 👥 4-Member Git Work Division Strategy
To prevent git merge conflicts, each team member owns a specific directory module:

| Member | Assigned Domain | Working Directory | Primary Responsibility |
|---|---|---|---|
| **Member 1** | **Frontend UI/UX** | `frontend/` | React 19 components, screens, theme, maps, responsive styling |
| **Member 2** | **Backend & API** | `backend/` | Express routes, auth, rate limiting, SLA sweeper, security |
| **Member 3** | **AI & ML Integration** | `ai/` | Gemini API, Claude failover, prompt engineering, entity extraction |
| **Member 4** | **Database & DevOps** | `database/`, `docker/`, `scripts/` | SQL schemas, seeds, Docker, deployment, documentation |

---

## 🚀 Status Tracker

### Completed ✅
- `[x]` Repository modularization into `frontend/`, `backend/`, `database/`, `ai/`, `admin/`, `shared/`, `mobile/`, `docker/`, `deployment/`, `.github/`.
- `[x]` Multi-provider AI failover ladder (Gemini → Bedrock → Claude → Static).
- `[x]` Passwordless OTP & Google OAuth 2.0 authentication.
- `[x]` Automated SLA breach sweeper background worker.
- `[x]` Interactive GIS map integration with location pinning.
- `[x]` Full documentation suite (23 root Markdown specifications).

### In Progress 🔄
- `[ ]` Live testing of MSG91 SMS gateway integration.
- `[ ]` Neon Postgres live connection verification.

### Future Improvements 🔮
- `[ ]` Offline PWA sync for remote field officers.
- `[ ]` Native WhatsApp bot interface for grievance filing.

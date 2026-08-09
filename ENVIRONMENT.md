# ⚙️ Environment Variables Guide — CivicAI

Complete list of environment variables used by CivicAI (from `.env.example`).

---

| Variable | Required | Default | Description |
|---|---|---|---|
| `AI_API_KEY` | **Yes** | — | Google Gemini API key for complaint triaging |
| `AI_MODEL` | No | `gemini-3.1-flash-lite` | Default Gemini model |
| `ANTHROPIC_API_KEY` | No | — | Optional Claude failover API key |
| `CLAUDE_MODEL` | No | `claude-haiku-4-5-20251001` | Default Claude failover model |
| `PORT` | No | `8787` | Express backend port |
| `AUTH_DEV_OTP` | No | `true` | Exposes OTP in response during development |
| `DATABASE_URL` | No | In-Memory | Neon Postgres connection string |
| `SESSION_SECRET` | Production | Ephemeral | Secret key for signing session cookies |
| `GOOGLE_CLIENT_ID` | No | — | Google OAuth client ID (server validation) |
| `VITE_GOOGLE_CLIENT_ID` | No | — | Google OAuth client ID (frontend rendering) |
| `SMS_ENABLED` | No | `false` | Set `true` to enable real MSG91 SMS sending |
| `MSG91_AUTH_KEY` | No | — | MSG91 SMS auth key |
| `MSG91_TEMPLATE_ID` | No | — | MSG91 DLT-approved OTP template ID |

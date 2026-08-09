# ❓ Frequently Asked Questions (FAQ) — CivicAI

### Q1: What happens if the Gemini API quota runs out?
**A**: CivicAI features an automatic multi-provider failover ladder: Gemini → AWS Bedrock (Claude) → Anthropic Claude Direct → Static Fallback. The app never breaks or crashes.

### Q2: How does OTP sign-in work in local development without SMS credits?
**A**: When `SMS_ENABLED` is not configured, the backend automatically runs in `console` mode. During local development (`NODE_ENV !== 'production'`), the generated 6-digit code is returned in the API response and displayed directly on the UI banner with a one-click **"Use this code"** auto-fill button.

### Q3: How are citizens' sensitive phone numbers protected?
**A**: Phone numbers are stored in normalized E.164 format and masked on the frontend (e.g. `+91 98•••••210`). OTPs are stored exclusively as SHA-256 hashes and compared using `timingSafeEqual`.

### Q4: Does the admin portal leak into public bundles?
**A**: No. The admin portal (`/portal/admin`) is isolated behind a lazy-loaded `React.lazy()` chunk boundary and guarded by `RequireAdmin.tsx` and backend RBAC rules.

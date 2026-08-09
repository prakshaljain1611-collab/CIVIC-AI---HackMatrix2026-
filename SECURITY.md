# 🛡️ Security Architecture — CivicAI

## 🔐 1. Authentication Security
- **Passwordless OTP**: 6-digit cryptographically random OTPs generated via `crypto.randomInt(100000, 1000000)`.
- **Timing-Safe Verification**: Hashes are stored as SHA-256 strings and compared using `crypto.timingSafeEqual`.
- **Exponential Lockout**: 9 wrong OTP attempts trigger a mandatory 15-minute account lockout.
- **Session Security**: `httpOnly`, `SameSite=Lax`, `Secure` cookies with uniform latency floor (450ms) to prevent timing side-channel attacks.

## 🤖 2. AI Key Isolation & Guardrails
- **Zero Frontend Leakage**: All AI API calls are proxy-handled on the Express backend (`backend/providers.ts`). AI keys are NEVER shipped to client JavaScript.
- **Strict Budget Limits**: Clamped to 2,000 input chars, 512 output tokens, and 60 requests/session daily cap.

## 🛡️ 3. Anti-Bot & Rate Limiting
- **Honeypot Trap**: Invisible form fields catch automated spambots.
- **Rate Limiters**: Fixed-window rate limiters for OTP requests (10 / 15m), verification (20 / 15m), and AI chat (15 / min).

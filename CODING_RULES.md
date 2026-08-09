# 📜 Coding Standards & Guidelines — CivicAI

## TypeScript Rules
1. **Strict Types**: Avoid `any` where possible. Use explicit interface definitions in `frontend/src/types.ts` and `backend/store.ts`.
2. **ESM Modules**: Use `.js` extension in relative imports for Node.js ESM compliance (`import { auth } from './auth.js'`).
3. **No Direct Secret Commits**: Keep API keys in `.env`.

## Frontend (React 19) Rules
1. **Component Scoping**: Small, focused components inside `frontend/src/components/`.
2. **Accessible Form Inputs**: Always pair `<input>` with `<label>` and `aria-describedby`.
3. **Lazy Loading**: Admin portal pages MUST be lazy-loaded (`React.lazy()`) so administrative code never leaks into public bundles.

## Backend (Express) Rules
1. **Timing Safety**: Use `crypto.timingSafeEqual` for security token comparisons.
2. **Sanitize Input**: Body parameters MUST be clamped and typed before processing.
3. **Error Handling**: Use `safeError` helper to avoid leaking stack traces in production.

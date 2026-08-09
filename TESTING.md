# 🧪 Testing & Verification Guide — CivicAI

## 🛠️ Automated Testing Commands

```bash
# 1. Type Checking & Static Linting
npm run lint

# 2. Production Build Verification
npm run build

# 3. Development Environment Doctor
npm run doctor

# 4. Dry-run Database Seed Test
npm run db:seed:dry
```

## 🔍 Validation Suite Coverage
- **Frontend Type Safety**: `tsc --noEmit` validates all React 19 JSX components and context state contracts.
- **Vite Bundle Splitting**: Ensures vendor chunks (`charts`, `maps`, `motion`, `icons`, `react`) build without circular dependencies.
- **Backend API Routes**: Exercised via `npm run doctor` and `npm run dev:full`.

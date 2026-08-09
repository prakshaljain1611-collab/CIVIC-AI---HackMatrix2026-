# 🗄️ Database Architecture — CivicAI

## Technology Choice
- **Primary Database**: PostgreSQL 14+ (tested on Neon Serverless Postgres).
- **Development Fallback**: In-memory PGlite or in-memory TypeScript store (`backend/store.ts`).

---

## Key Domain Tables

### 1. `users`
Stores citizen and administrative user accounts.
- `id` (UUID, Primary Key)
- `phone` (TEXT, E.164 format, Unique)
- `email` (TEXT, Unique)
- `full_name` (TEXT)
- `role_id` (FK → `roles.id`)
- `status` (ENUM: `active`, `suspended`, `pending`, `deactivated`)

### 2. `complaints`
Central repository for submitted grievances.
- `id` (UUID, Primary Key)
- `tracking_id` (TEXT, Unique format `CIV-YYYYMMDD-XXXX`)
- `citizen_id` (FK → `users.id`)
- `title` & `description` (TEXT)
- `category` (ENUM: Road, Water, Electricity, Sanitation, Law & Order, Transport, Parks, General)
- `priority` (ENUM: Low, Medium, High, Critical)
- `status` (ENUM: submitted, ai_verification, department_assigned, officer_assigned, investigation_started, work_in_progress, resolved, closed)
- `latitude` & `longitude` (DOUBLE PRECISION)
- `location_address` (TEXT)
- `sla_expires_at` (TIMESTAMPTZ)
- `sla_breached` (BOOLEAN)

### 3. `audit_logs`
Tracks immutability of system actions for accountability.
- `id` (UUID)
- `actor_id` (FK → `users.id`)
- `action` (TEXT)
- `entity_type` & `entity_id` (TEXT)
- `created_at` (TIMESTAMPTZ)

---

## Seed & Migration Commands
```bash
# Run database seed
npm run db:seed

# Reset database schema and seed data
npm run db:reset
```
Schema SQL files: [`database/001_schema.sql`](file:///Users/himanshusingh/Downloads/CIVI-AI-PRJ-main/database/001_schema.sql) and [`database/002_rls.sql`](file:///Users/himanshusingh/Downloads/CIVI-AI-PRJ-main/database/002_rls.sql).

# 🏛️ Admin & Staff Portal Module

This module documents administrative workflows, officer dashboards, grievance assignment, and RBAC authorization policies.

---

## 🎯 Scope & Features
- **Role-Based Access Control (RBAC)**: Supports `super_admin`, `department_head`, `field_officer`, and `auditor`.
- **Live Complaint Management**: Filterable complaint drawer with real-time status updates via Server-Sent Events (`/api/events`).
- **SLA Breach Warnings**: Visual indicators for complaints nearing SLA limits.
- **Automated Official Responses**: AI-assisted template generation for official status letters.

---

## 📁 Key Files
- Admin Frontend Dashboard: `frontend/src/components/admin/AdminPortal.tsx`
- Admin Complaint Drawer: `frontend/src/components/admin/ComplaintDrawer.tsx`
- Admin Auth Guard: `frontend/src/portals/RequireAdmin.tsx`
- Admin Backend API Router: `backend/admin.ts`
- RBAC Rules Engine: `backend/rbac.ts`

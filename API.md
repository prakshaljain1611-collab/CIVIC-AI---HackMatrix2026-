# 🔌 REST API Documentation — CivicAI

Base URL: `http://localhost:8787/api`

---

## 🔑 Authentication Endpoints

### 1. Request OTP
- **POST** `/api/auth/request-otp`
- **Rate Limit**: 10 requests / 15 min
- **Body**: `{ "identifier": "+919876543210" }`
- **Response**:
```json
{
  "ok": true,
  "channel": "phone",
  "maskedIdentifier": "+91 98•••••210",
  "expiresInSec": 300,
  "message": "Verification code sent."
}
```

### 2. Verify OTP
- **POST** `/api/auth/verify-otp`
- **Rate Limit**: 20 requests / 15 min
- **Body**: `{ "identifier": "+919876543210", "otp": "905869" }`
- **Response**: Sets `session` httpOnly cookie.

### 3. Check Session
- **GET** `/api/auth/session`
- **Headers**: Cookie / `Authorization: Bearer <token>`

---

## 🤖 AI & Complaint Endpoints

### 4. AI Chat Assistant
- **POST** `/api/chat`
- **Rate Limit**: 15 requests / min
- **Body**: `{ "message": "Pothole near Sector 18 Noida", "history": [] }`
- **Response**: Structured reply, category, priority, sentiment, and location coordinates.

### 5. Analyze Complaint
- **POST** `/api/analyze-complaint`
- **Rate Limit**: 10 requests / min
- **Body**: `{ "title": "Water leakage", "description": "Pipe burst on main road" }`
- **Response**: Category, priority, sentiment, estimated resolution time.

### 6. Complaints List / Create
- **GET** `/api/complaints`
- **POST** `/api/complaints`

---

## 📊 System Health & Events
- **GET** `/api/health` — Provider status, SMS provider, store provider, version.
- **GET** `/api/events` — Server-Sent Events (SSE) for real-time dashboard updates.

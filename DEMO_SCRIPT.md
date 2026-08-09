# 🎬 Live Presentation & Demo Script — CivicAI

**Duration**: 5–7 Minutes  
**Target Audience**: HackMatrix 2K26 Judges & Evaluation Panel

---

## 🕒 Minute 0:00 – 1:00 | The Problem & Context
> *"Good morning judges! Every day, millions of citizens file grievances on public portals. But manual triaging creates massive backlogs, wrong department routing, and missed SLA deadlines. Today we present **CivicAI: Jansunwai Portal 2.0**."*

## 🕒 Minute 1:00 – 2:30 | Citizen Intake & Passwordless Auth
1. **Show Citizen Portal**: Open [https://civic-ai-hack-matrix2026.vercel.app](https://civic-ai-hack-matrix2026.vercel.app) (or local `http://localhost:3000`).
2. **Demonstrate OTP Sign-In**: Enter phone number, click send. Show how the dev banner displays code `905869` with the **"Use this code"** auto-fill button.
3. **Conversational Intake**: Type *"Water pipeline burst on MG Road near Sector 18"*.
4. **Point out AI Output**: Show how Gemini automatically categorizes it under **Water Supply**, marks priority as **High**, extracts **Sector 18**, and drops a pinpoint pin on the GIS map!

## 🕒 Minute 2:30 – 4:30 | Staff Portal & Real-time SLA Sweeper
1. **Navigate to Staff Portal**: Open `/portal/admin`.
2. **Live Feed**: Point out how the newly filed grievance immediately appeared in the officer's live feed via Server-Sent Events (SSE).
3. **SLA Countdown**: Highlight the real-time SLA timer and breach sweeper status.
4. **AI Response Generation**: Click **Generate Official Response** to show instant AI drafting of status letters.

## 🕒 Minute 4:30 – 5:30 | Security & Tech Stack Summary
1. Highlight zero API key leakage (100% server proxy).
2. Show multi-provider failover (Gemini → Bedrock → Claude).
3. Conclude with impact stats!

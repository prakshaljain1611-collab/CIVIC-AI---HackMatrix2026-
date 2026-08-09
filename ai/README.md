# 🤖 AI & Machine Learning Module (Member 3 Domain)

This directory contains the AI/LLM models, prompt templates, triaging rules, and provider failover strategies for **CivicAI**.

---

## 👨‍💻 Primary Owner
**Member 3 — AI / LLM Integration Lead**

---

## 🎯 Scope & Responsibilities
1. **Multi-Provider Failover Pipeline**:
   - **Primary**: Google Gemini API (`gemini-3.1-flash-lite`) for high-throughput, structured JSON triaging.
   - **Fallback Policy**: Gemini 3.1 Flash → AWS Bedrock (Claude) → Anthropic Claude Direct → Static Fallback.
   - **Quota Monitoring**: Built-in sliding-window rate limiters and daily global caps.
   - **Fallback 2**: Anthropic Claude Direct API (`claude-haiku-4-5-20251001`).
   - **Fallback 3**: Static fallback response ladder ensuring 100% uptime.

2. **Automated Grievance Classification**:
   - Categorization into 8 civic departments: *Road & Infrastructure*, *Water Supply*, *Electricity*, *Sanitation*, *Law & Order*, *Public Transport*, *Parks & Recreation*, *General*.
   - Severity & Priority Scoring (*Low*, *Medium*, *High*, *Critical*).
   - Citizen sentiment analysis (*Frustrated*, *Neutral*, *Polite*, *Angry*).

3. **Geospatial & Entity Extraction**:
   - Extraction of location landmarks, sector numbers, and street names.
   - GIS coordinate mapping relative to city center.

---

## 📁 Key Files
- Core AI Engine implementation: `backend/providers.ts`
- Conversational Intake & Prompt Templates: `backend/chat.ts`
- Duplicate Detection Algorithms: `backend/duplicates.ts`
- AI Usage & Quota Guards: `backend/limits.ts`

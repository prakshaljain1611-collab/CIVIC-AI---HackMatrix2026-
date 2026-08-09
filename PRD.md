# 📄 Product Requirement Document (PRD) — CivicAI

## 1. Problem Statement
Municipal grievance systems (like Jansunwai) face severe operational challenges:
- Manual triaging causes delays, backlog buildup, and incorrect department routing.
- Citizens lack transparent, real-time tracking and SLA visibility.
- High rates of spam/duplicate filings waste administrative capacity.
- Lack of automated status communication creates frustration.

## 2. Target Users
1. **Citizens**: Indian residents reporting public infrastructure, sanitation, law & order, or utility issues.
2. **Department Officials / Field Officers**: Municipal staff responsible for investigating and resolving assigned complaints within SLA deadlines.
3. **Super Administrators / Auditors**: Senior officials monitoring city-wide complaint resolution metrics, SLA breach rates, and department performance.

## 3. Core Goals
- **Automated AI Triaging**: Classify complaints into 8 departments, extract location entities, and assign priority scores in < 2 seconds.
- **SLA Guarantee**: Enforce strict resolution timers (Critical: 24h, High: 48h, Medium: 72h, Low: 120h) with background breach alerts.
- **Accessible & Passwordless Auth**: Google OAuth + Phone/SMS OTP login without complex password requirements.
- **Duplicate & Fraud Prevention**: Contextual duplicate detection and anti-bot honeypots.

## 4. Non-Goals
- Replacing human authority: AI recommends priority/department, but officers retain full authority to override.
- Hardware sensor telemetry: Integration is software and API driven.

## 5. Success Criteria
- > 90% reduction in complaint routing time.
- 0% missed SLA warnings due to real-time sweepers.
- WCAG AAA compliance for maximum accessibility across devices.

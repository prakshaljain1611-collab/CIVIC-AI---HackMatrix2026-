# 📜 Changelog — CivicAI

All notable changes to **CivicAI** are documented in this file.

---

## [2.0.0] - 2026-08-09
### Added
- Complete repository modularization into 4-member clear domains (`frontend/`, `backend/`, `database/`, `ai/`).
- Multi-provider AI failover architecture (Gemini → AWS Bedrock → Claude → Static).
- Automatic SLA breach sweeper running on 5-minute background intervals.
- Passwordless OTP auth supporting dev console mode auto-display.
- Complete 23-file documentation suite compliant with HackMatrix 2K26 guidelines.

### Changed
- Refactored `src/` to `frontend/src/` and `server/` to `backend/`.
- Updated package scripts and build entrypoints for zero-downtime development (`npm run dev:full`).

### Fixed
- Fixed dev OTP code accessibility in local development.

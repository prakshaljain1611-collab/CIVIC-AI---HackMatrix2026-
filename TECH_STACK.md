# 💻 Technology Stack — CivicAI

Only technologies actively implemented in this repository are listed:

## Frontend Stack
- **React 19** (`^19.0.1`): UI component rendering library.
- **TypeScript** (`~5.8.2`): Type safety and interface contracts.
- **Vite** (`^6.2.3`): Ultra-fast frontend bundler and development server.
- **TailwindCSS v4** (`^4.1.14`): Utility-first CSS engine.
- **Framer Motion / Motion** (`^12.43.0`): Smooth micro-animations.
- **Leaflet & React-Leaflet** (`^1.9.4` / `^5.0.0`): Open-source interactive GIS map views.
- **Recharts** (`^3.8.1`): Admin analytics data visualizations.
- **Lucide React** (`^0.546.0`): Accessible SVG icons.
- **OGL** (`^1.0.11`): WebGL background shader rendering.

## Backend Stack
- **Node.js & Express** (`^4.21.2`): Server-side HTTP REST API.
- **tsx** (`^4.21.0`): Zero-build TypeScript execution engine.
- **dotenv** (`^17.2.3`): Environment variable loader.

## AI & ML Integration
- **@google/genai** (`^1.29.0`): Primary LLM SDK for Gemini 3.1 Flash Lite.
- **AWS Bedrock / Anthropic SDK**: Failover LLM providers.

## Database & Persistence
- **@neondatabase/serverless** (`^1.1.0`): Serverless PostgreSQL driver.
- **@electric-sql/pglite** (`^0.5.4`): In-memory WASM PostgreSQL for local development and testing.

## Authentication & SMS Providers
- **Google Auth Library** (`^10.9.1`): Google One-Tap & OAuth 2.0 credential verification.
- **MSG91 / Twilio**: SMS OTP gateway support (Console mode fallback for dev).

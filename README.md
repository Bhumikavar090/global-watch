# 🌍 Global Watch

**Global Watch** is a real-time geopolitical intelligence and situational-awareness platform that combines interactive 3D/2D maps, live OSINT feeds, financial data, threat intelligence, and AI-powered analysis into a unified dashboard.

It aggregates information from multiple live data sources and transforms raw signals into actionable intelligence through automated correlation, risk scoring, hotspot detection, and LLM-powered summaries.

## ✨ Key Features

* 🗺️ **Dual Map Engine** — Switch between interactive 3D globe and WebGL-based 2D maps with 45+ shared data layers.
* 🤖 **AI-Powered Intelligence** — LLM-generated summaries, RAG-based intelligence retrieval, threat classification, and country-level analysis.
* 📰 **Live OSINT Monitoring** — Aggregates 435+ RSS feeds, live video streams, webcams, Telegram/OSINT channels, and keyword monitors.
* 🚨 **Threat & Risk Detection** — Signal aggregation, hotspot escalation, country instability analysis, and strategic risk scoring.
* 📈 **Financial Intelligence** — Market, cryptocurrency, energy, macroeconomic, and investment data analysis.
* 🖥️ **Cross-Platform** — Web/PWA experience with a native desktop application powered by Tauri and Rust.
* 🌐 **Internationalization** — 21-language support with RTL compatibility.
* ⚡ **Performance & Caching** — Redis, IndexedDB, service workers, and CDN-based caching for efficient data delivery.

## 🧠 Intelligence Pipeline

```text
┌─────────────────────────────────────────────────────┐
│                  LIVE DATA SOURCES                   │
│  News • OSINT • Markets • Satellites • Threat Intel │
└───────────────────────┬─────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────┐
│                DATA INGESTION LAYER                  │
│     APIs • RSS • ADS-B • Satellite • Telegram       │
└───────────────────────┬─────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────┐
│             SIGNAL PROCESSING & CORRELATION          │
│   Aggregation • Classification • Deduplication       │
│   Hotspot Detection • Risk Scoring • Correlation     │
└───────────────────────┬─────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────┐
│                    AI / RAG LAYER                    │
│      Embeddings • Retrieval • LLM Analysis          │
│       Summarization • Threat Classification         │
└───────────────────────┬─────────────────────────────┘
                        │
                        ▼
┌─────────────────────────────────────────────────────┐
│                 GLOBAL WATCH DASHBOARD               │
│   Maps • News • Intelligence • Markets • Alerts     │
└─────────────────────────────────────────────────────┘
```

## 🛠️ Tech Stack

### Frontend

* TypeScript
* React
* Vite
* Three.js
* globe.gl
* MapLibre GL
* deck.gl

### Desktop

* Tauri 2
* Rust
* Node.js sidecar
* OS keychain integration

### AI / ML

* Ollama
* LM Studio
* Groq
* OpenRouter
* Transformers.js
* RAG
* IndexedDB vector storage

### Backend & Infrastructure

* Node.js
* Redis / Upstash
* Protocol Buffers
* OpenAPI 3.1
* Service Workers
* Vercel
* Railway

## 🌐 Data Sources

Global Watch integrates multiple categories of real-time and historical data.

### Geopolitical & OSINT

* OpenSky
* GDELT
* ACLED
* UCDP
* HAPI
* USGS
* GDACS
* NASA EONET
* NASA FIRMS
* Cloudflare Radar
* WorldPop
* Telegram/OSINT sources

### Markets & Finance

* Yahoo Finance
* CoinGecko
* mempool.space
* Alternative.me
* FRED
* EIA
* Finnhub

### Threat Intelligence

* abuse.ch
* AlienVault OTX
* AbuseIPDB
* C2IntelFeeds

## 📊 Intelligence Coverage

* **45+** interactive data layers
* **435+** RSS feeds
* **30+** live video channels
* **22** live webcams
* **21** supported languages
* **92** stock exchanges
* **19** financial centers
* **13** central banks
* **10** commodity hubs
* **64** Gulf FDI investments

## 📁 Project Structure

```text
global-watch/
├── api/              # API and service integrations
├── blog-site/        # Blog/content application
├── convex/           # Data/backend functionality
├── data/             # Data processing and datasets
├── deploy/           # Deployment configuration
├── docker/           # Docker configuration
├── docs/             # Documentation
├── e2e/              # End-to-end tests
├── proto/            # Protocol Buffer definitions
├── public/            # Static assets
├── scripts/           # Utility and automation scripts
├── server/            # Server-side functionality
├── shared/            # Shared types and utilities
├── src/               # Main frontend application
├── src-tauri/         # Tauri desktop application
├── tests/             # Test suites
├── .env.example       # Environment variable template
├── index.html
├── package.json
└── README.md
```

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

* Node.js
* npm
* Git

For the desktop application:

* Rust
* Tauri CLI

### Installation

Clone the repository:

```bash
git clone https://github.com/Bhumikavar090/global-watch.git
cd global-watch
```

Install dependencies:

```bash
npm install
```

Create your local environment file:

```bash
cp .env.example .env
```

Add the required API keys and service configuration to `.env`.

### Development

Start the development server:

```bash
npm run dev
```

The application should then be available through the local development URL displayed by Vite.

### Desktop Development

If the Tauri desktop environment is configured:

```bash
npm run tauri dev
```

> Available scripts may vary depending on the current project configuration. Run `npm run` to view all available commands.

## 🔐 Environment Variables

Global Watch uses multiple external APIs and services. **Never commit real API keys or credentials to GitHub.**

Use `.env.example` as a template for local configuration.

Example:

```env
VITE_GROQ_API_KEY=
VITE_OPENROUTER_API_KEY=
VITE_REDIS_URL=
```

The exact environment variables required depend on the enabled data providers and application modules.

## ⚡ Performance

Global Watch uses multiple layers of caching and client-side optimization to reduce unnecessary API requests and improve responsiveness:

* Redis / Upstash caching
* Vercel CDN
* Service Worker caching
* IndexedDB persistence
* Client-side vector storage
* Lazy-loaded data layers
* Shared map data architecture

## 🔌 API Architecture

The project follows a contract-first approach for API development.

```text
Protocol Buffers
       ↓
Generated Contracts
       ↓
TypeScript Clients / Servers
       ↓
Application Services
       ↓
External Data Providers
```

OpenAPI 3.1 documentation is used for API discoverability and integration.

## 🤖 AI Architecture

The AI layer supports both local and cloud-based models.

```text
Raw Intelligence
       ↓
Preprocessing
       ↓
Embedding / Indexing
       ↓
Vector Retrieval
       ↓
Relevant Context
       ↓
LLM
       ↓
Summary / Analysis / Classification
```

This enables the platform to combine current events with previously indexed intelligence instead of relying solely on the model's static knowledge.

## 🖥️ Platform Support

| Platform      | Support         |
| ------------- | --------------- |
| Web           | ✅               |
| PWA           | ✅               |
| Desktop       | ✅ Tauri         |
| Mobile        | ✅ Responsive UI |
| 3D Globe      | ✅               |
| 2D WebGL Map  | ✅               |
| RTL Languages | ✅               |

## 🔒 Security

The project is designed with security considerations including:

* Environment-based secret management
* Authentication and authorization where required
* API boundary separation
* OS keychain integration for desktop credentials
* No hardcoded production credentials
* Controlled access to external services

## 📌 Project Status

Global Watch is an actively developed intelligence dashboard and research project. Data availability and functionality may vary depending on the availability and rate limits of external APIs.

## 👥 Team

Developed as a **4-member team project**, with contributions across application development, data integration, AI functionality, and platform engineering.

## 📄 License

This project is currently maintained as a personal/academic project.

If a formal open-source license is added, update this section accordingly.

---

### ⭐ Project Highlights

> **Global Watch transforms hundreds of live information streams into a unified intelligence interface combining geospatial visualization, OSINT, financial data, threat intelligence, and AI-powered analysis.**

**Built with TypeScript • React • Three.js • MapLibre • Node.js • Rust • Tauri • LLMs • RAG • Redis**

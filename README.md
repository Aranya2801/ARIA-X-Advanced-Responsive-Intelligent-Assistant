<div align="center">

```
  █████╗ ██████╗ ██╗ █████╗     ██╗  ██╗
 ██╔══██╗██╔══██╗██║██╔══██╗    ╚██╗██╔╝
 ███████║██████╔╝██║███████║     ╚███╔╝ 
 ██╔══██║██╔══██╗██║██╔══██║     ██╔██╗ 
 ██║  ██║██║  ██║██║██║  ██║    ██╔╝ ██╗
 ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝╚═╝  ╚═╝   ╚═╝  ╚═╝
```

# ARIA X — Advanced Responsive Intelligent Assistant

**A production-grade, JARVIS-like AI voice companion — 2026 Edition**

[![Python](https://img.shields.io/badge/Python-3.12+-00d4ff?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.115-00d4ff?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React-18.3-00d4ff?style=for-the-badge&logo=react&logoColor=white)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.4-00d4ff?style=for-the-badge&logo=typescript&logoColor=white)](https://typescriptlang.org)
[![Docker](https://img.shields.io/badge/Docker-Ready-00d4ff?style=for-the-badge&logo=docker&logoColor=white)](https://docker.com)
[![License](https://img.shields.io/badge/License-MIT-7c3aed?style=for-the-badge)](LICENSE)

*"The future of personal AI — intelligent, empathetic, always ready."*

---

</div>

## ✨ What is ARIA X?

ARIA X is a **futuristic, production-ready AI voice assistant** that combines the capabilities of ChatGPT, Claude, JARVIS, and Siri into a single premium application. Built with a **multi-agent architecture**, real-time voice interaction, persistent memory, and a stunning cyberpunk UI — ARIA X is designed to feel like a real AI companion from a sci-fi movie.

### 🎯 Core Experience

When you launch ARIA X:

> *"Hello. This is ARIA. Your personal AI assistant. How may I assist you today?"*

On first launch:

> *"Hello. This is ARIA. Before we begin, may I know your name please?"*

After you respond:

> *"Wonderful to meet you, Aranya. I am ready whenever you need me."*

Every future session:

> *"Welcome back, Aranya. I hope you're having a great day. How may I help you?"*

---

## 🌟 Feature Highlights

| Category | Features |
|----------|----------|
| 🎙️ **Voice** | ElevenLabs TTS, Whisper STT, Deepgram, Azure Neural, Wake Word Detection |
| 🧠 **AI** | GPT-4o + Claude fallback, multi-agent routing, chain-of-thought reasoning |
| 💾 **Memory** | ChromaDB vector search, long-term SQL memory, short-term session context |
| 👁️ **Vision** | GPT-4V image analysis, OCR, screenshot reading, chart analysis |
| 🤖 **Agents** | 8 specialist agents: Research, Coding, Document, Task, Planning, Vision, Memory |
| 🔍 **Research** | Real-time web search, article summarization, trend analysis |
| 🎨 **UI** | Glassmorphism, cyberpunk HUD, particle effects, animated waveforms |
| 🔐 **Security** | JWT auth, bcrypt, rate limiting, security headers, session management |
| 📊 **Observability** | Prometheus metrics, Grafana dashboards, structured logging |
| 🐳 **Deployment** | Docker Compose, Nginx, GitHub Actions CI/CD, Kubernetes-ready |

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                          ARIA X Architecture                         │
├─────────────────────────────────────────────────────────────────────┤
│                                                                       │
│  ┌──────────────────────────────────────────────────────────────┐   │
│  │                    Frontend (React + Vite)                    │   │
│  │  ┌────────────┐  ┌────────────┐  ┌──────────┐  ┌─────────┐  │   │
│  │  │ ARIA Core  │  │ Chat Panel │  │ HUD + FX │  │ SideBar │  │   │
│  │  │  (Orb UI)  │  │  (Stream)  │  │(Particle)│  │(Agents) │  │   │
│  │  └────────────┘  └────────────┘  └──────────┘  └─────────┘  │   │
│  └──────────────────────────────────────────────────────────────┘   │
│                       │ WebSocket / REST API │                        │
│  ┌──────────────────────────────────────────────────────────────┐   │
│  │                   Backend (FastAPI + Python)                  │   │
│  │  ┌──────────────────────────────────────────────────────┐   │   │
│  │  │                  Agent Orchestrator                   │   │   │
│  │  │  ┌──────────┐  ┌──────────┐  ┌───────┐  ┌────────┐  │   │   │
│  │  │  │Conversat.│  │ Research │  │Coding │  │Document│  │   │   │
│  │  │  └──────────┘  └──────────┘  └───────┘  └────────┘  │   │   │
│  │  │  ┌──────────┐  ┌──────────┐  ┌───────┐  ┌────────┐  │   │   │
│  │  │  │  Memory  │  │  Vision  │  │  Task │  │Planning│  │   │   │
│  │  │  └──────────┘  └──────────┘  └───────┘  └────────┘  │   │   │
│  │  └──────────────────────────────────────────────────────┘   │   │
│  │  ┌──────────────┐  ┌─────────────┐  ┌────────────────────┐  │   │
│  │  │ Voice Engine │  │Memory Mgr   │  │  Security Layer    │  │   │
│  │  │ ElevenLabs   │  │ChromaDB+SQL │  │  JWT + Rate Limit  │  │   │
│  │  │ Whisper/DG   │  │FAISS + Redis│  │  Bcrypt + Headers  │  │   │
│  │  └──────────────┘  └─────────────┘  └────────────────────┘  │   │
│  └──────────────────────────────────────────────────────────────┘   │
│                                                                       │
│  ┌────────────┐  ┌────────────┐  ┌────────────┐  ┌──────────────┐  │
│  │ PostgreSQL │  │   Redis    │  │  ChromaDB  │  │  Prometheus  │  │
│  │  (SQL DB)  │  │  (Cache)   │  │ (Vectors)  │  │  + Grafana   │  │
│  └────────────┘  └────────────┘  └────────────┘  └──────────────┘  │
└─────────────────────────────────────────────────────────────────────┘
```

---

## 📁 Project Structure

```
ARIA-X/
├── backend/                          # FastAPI Python backend
│   ├── main.py                       # App entry point
│   ├── requirements.txt              # Python dependencies
│   ├── Dockerfile                    # Backend container
│   ├── api/
│   │   ├── websocket.py              # Real-time WS handler
│   │   └── routes/
│   │       ├── auth.py               # JWT authentication
│   │       ├── chat.py               # Chat REST endpoint
│   │       ├── voice.py              # TTS / STT endpoints
│   │       ├── agents.py             # Agent status
│   │       ├── memory.py             # Memory CRUD
│   │       ├── vision.py             # Image analysis
│   │       └── system.py             # Health & info
│   ├── agents/
│   │   ├── base.py                   # Base agent class
│   │   ├── orchestrator.py           # Agent router
│   │   ├── conversation_agent.py     # Primary chat (GPT-4o)
│   │   ├── research_agent.py         # Web search + RAG
│   │   ├── coding_agent.py           # Code generation
│   │   ├── document_agent.py         # Document creation
│   │   ├── task_agent.py             # Tasks & reminders
│   │   ├── memory_agent.py           # Memory operations
│   │   ├── vision_agent.py           # Image understanding
│   │   └── planning_agent.py         # Multi-step planning
│   ├── memory/
│   │   ├── database.py               # SQLAlchemy models + init
│   │   └── manager.py                # Memory CRUD + vector search
│   ├── voice/
│   │   └── engine.py                 # TTS + STT + Wake word
│   ├── security/
│   │   └── middleware.py             # Rate limit + security headers
│   └── utils/
│       ├── config.py                 # Pydantic settings
│       └── logger.py                 # Structured logging
│
├── frontend/                         # React TypeScript frontend
│   ├── src/
│   │   ├── main.tsx                  # Entry point
│   │   ├── App.tsx                   # Root with routing
│   │   ├── index.css                 # Glassmorphism + HUD styles
│   │   ├── pages/
│   │   │   ├── LoginPage.tsx         # Auth UI
│   │   │   ├── OnboardingPage.tsx    # First-time setup
│   │   │   └── MainDashboard.tsx     # Main JARVIS interface
│   │   ├── components/
│   │   │   ├── voice/ARIACore.tsx    # Animated AI orb
│   │   │   ├── dashboard/
│   │   │   │   ├── ChatPanel.tsx     # Streaming messages
│   │   │   │   ├── InputBar.tsx      # Text + voice input
│   │   │   │   ├── StatusBar.tsx     # Top HUD bar
│   │   │   │   └── SidePanel.tsx     # Left sidebar
│   │   │   └── effects/
│   │   │       ├── ParticleCanvas.tsx # Animated particles
│   │   │       └── HUDOverlay.tsx    # Cyberpunk HUD
│   │   ├── hooks/
│   │   │   ├── useWebSocket.ts       # WS + streaming
│   │   │   └── useVoiceRecorder.ts   # MediaRecorder API
│   │   └── store/
│   │       ├── authStore.ts          # Zustand auth
│   │       └── ariaStore.ts          # Zustand ARIA state
│   └── package.json
│
├── infrastructure/
│   ├── nginx/nginx.conf              # Reverse proxy config
│   └── monitoring/prometheus.yml    # Metrics scraping
│
├── tests/
│   ├── unit/test_core.py             # Unit tests
│   └── integration/test_api.py      # API integration tests
│
├── scripts/
│   ├── setup.sh                      # One-time setup
│   ├── start-dev.sh                  # Dev servers
│   └── start-docker.sh               # Docker start
│
├── data/
│   └── migrations/env.py             # Alembic config
│
├── .env.example                      # Environment template
├── docker-compose.yml                # Full stack orchestration
├── pytest.ini                        # Test config
└── README.md                         # This file
```

---

## 🚀 Quick Start

### Prerequisites

- Python 3.12+
- Node.js 20+
- Docker + Docker Compose (optional but recommended)
- At minimum: **OpenAI API key**

### Option A — Local Development (Fastest)

```bash
# 1. Clone the repository
git clone https://github.com/Aranya2801/ARIA-X.git
cd ARIA-X

# 2. Run setup (creates .env, installs deps)
chmod +x scripts/setup.sh
./scripts/setup.sh

# 3. Add your API keys to .env
nano .env
# Required: OPENAI_API_KEY=sk-...
# Optional: ELEVENLABS_API_KEY, DEEPGRAM_API_KEY, ANTHROPIC_API_KEY

# 4. Start both servers
./scripts/start-dev.sh

# 5. Open http://localhost:3000
```

### Option B — Docker Compose (Recommended for production)

```bash
# 1. Clone & configure
git clone https://github.com/Aranya2801/ARIA-X.git
cd ARIA-X
cp .env.example .env
nano .env  # add your API keys

# 2. Launch everything
./scripts/start-docker.sh

# Services will be available at:
# App:        http://localhost
# API Docs:   http://localhost/api/docs
# Grafana:    http://localhost:3001  (admin / aria_grafana)
# Prometheus: http://localhost:9090
```

### Option C — Manual Setup

```bash
# Backend
cd backend
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8000

# Frontend (new terminal)
cd frontend
npm install
npm run dev
```

---

## 🔑 API Keys Setup

| Key | Where to get | Required |
|-----|-------------|----------|
| `OPENAI_API_KEY` | [platform.openai.com](https://platform.openai.com) | ✅ Yes |
| `ELEVENLABS_API_KEY` | [elevenlabs.io](https://elevenlabs.io) | For premium voice |
| `DEEPGRAM_API_KEY` | [deepgram.com](https://deepgram.com) | For better STT |
| `ANTHROPIC_API_KEY` | [console.anthropic.com](https://console.anthropic.com) | For Claude fallback |
| `AZURE_SPEECH_KEY` | [azure.microsoft.com](https://azure.microsoft.com) | For Azure TTS |

---

## 🎙️ Voice System

ARIA uses a layered voice architecture:

```
User Speech
    │
    ▼
Whisper STT (OpenAI)
    │  └── Deepgram fallback
    ▼
Wake Word Detection
    │  "hey aria" / "aria" / "assistant"
    ▼
Intent Classification → Agent Routing
    │
    ▼
LLM Response (GPT-4o → Claude fallback)
    │
    ▼
Emotion Detection
    │
    ▼
ElevenLabs TTS (Bella voice)
    │  └── Azure Neural TTS fallback
    ▼
Audio Stream → Browser Playback
```

### Voice Controls

| Action | How |
|--------|-----|
| Start listening | Click microphone button or say wake word |
| Stop listening | Click microphone button again |
| Toggle voice response | Click 🔊 button in input bar |
| Wake word | Say "Hey ARIA", "ARIA", or "Assistant" |

---

## 🤖 Agent System

ARIA routes every request to the best specialist agent:

| Agent | Triggers | Capabilities |
|-------|----------|-------------|
| **Conversation** | Default | Natural dialogue, Q&A, reasoning |
| **Research** | search, news, find, look up | Web search, summaries, fact-checking |
| **Coding** | code, debug, write function | Code generation, debugging, explanation |
| **Document** | write, draft, report, email | Documents, reports, emails, letters |
| **Task** | remind, todo, schedule | Task tracking, reminders, scheduling |
| **Memory** | remember, recall, note | Memory storage and retrieval |
| **Vision** | image, screenshot, analyze | Image analysis, OCR, chart reading |
| **Planning** | plan, roadmap, strategy | Multi-step planning, goal decomposition |

---

## 🧠 Memory System

ARIA remembers everything across sessions:

```
Short-Term Memory  →  In-process ring buffer (last 20 messages)
Long-Term Memory   →  PostgreSQL + ChromaDB vectors
Semantic Search    →  ChromaDB + FAISS similarity search
User Profile       →  Preferences, name, personality mode
```

Memory is automatically:
- **Stored** when you share information with ARIA
- **Retrieved** via semantic similarity when relevant
- **Ranked** by importance and access frequency
- **Consolidated** in background to remove duplicates

---

## 🎨 UI Design

The interface is inspired by:
- **JARVIS** (Iron Man) — HUD overlays, holographic displays
- **Cyberpunk 2077** — neon blue on dark backgrounds
- **Modern AI dashboards** — glassmorphism, clean data visualization

### Design System

```css
Colors:
  --aria-blue:    #00d4ff   (primary neon blue)
  --aria-cyan:    #00fff7   (accent cyan)
  --aria-purple:  #7c3aed   (secondary purple)
  --aria-bg:      #030712   (deep dark background)

Typography:
  Display:  Orbitron (futuristic headers)
  Body:     Inter (readable text)
  Code:     JetBrains Mono

Effects:
  - Glassmorphism panels (backdrop-filter: blur)
  - Particle canvas background
  - HUD corner decorations
  - Animated scan lines
  - Neon glow shadows
  - Real-time audio waveforms
```

---

## 📊 Monitoring

Access Grafana at `http://localhost:3001` (admin / aria_grafana) for:

- Request rate and latency per endpoint
- Agent usage distribution
- Voice session metrics
- Memory store growth
- Error rates and alerts
- System resource usage

---

## 🔒 Security

- **JWT authentication** with configurable expiry
- **bcrypt password hashing** (12 rounds)
- **Rate limiting** per IP (120 req/min API, 30 req/min behind Nginx)
- **Security headers** (HSTS, X-Frame-Options, CSP)
- **CORS** with explicit allowed origins
- **Encrypted secrets** via environment variables
- **Non-root Docker container**

---

## 🧪 Testing

```bash
# Run all tests
cd backend
pytest

# With coverage
pytest --cov=. --cov-report=html

# Specific test file
pytest tests/unit/test_core.py -v

# Integration tests
pytest tests/integration/ -v
```

---

## 🛣️ Roadmap

### MVP (Current)
- [x] Voice interaction (STT + TTS)
- [x] Multi-agent routing
- [x] Long-term memory
- [x] Real-time WebSocket streaming
- [x] Glassmorphism cyberpunk UI
- [x] JWT authentication
- [x] Docker deployment

### v2.1 — Near Term
- [ ] Wake word detection (Porcupine / Picovoice)
- [ ] Email agent (SMTP + IMAP)
- [ ] Google Calendar integration
- [ ] File upload and document parsing
- [ ] Multi-language support (10+ languages)

### v2.5 — Medium Term
- [ ] Computer control (PyAutoGUI + Playwright)
- [ ] Local LLM support (Ollama / Llama 3)
- [ ] Mobile app (React Native / Capacitor)
- [ ] Voice authentication (speaker recognition)
- [ ] Multi-user households

### v3.0 — Vision
- [ ] Fully autonomous agent workflows
- [ ] AR/VR holographic interface
- [ ] Predictive task execution
- [ ] Emotional intelligence layer
- [ ] Personal knowledge graph

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push: `git push origin feature/amazing-feature`
5. Open a Pull Request

Please follow the code style (Black + Ruff for Python, ESLint for TypeScript).

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

## 🙏 Acknowledgments

Built on the shoulders of giants:
- [OpenAI](https://openai.com) — GPT-4o, Whisper
- [Anthropic](https://anthropic.com) — Claude (fallback)
- [ElevenLabs](https://elevenlabs.io) — Neural TTS
- [FastAPI](https://fastapi.tiangolo.com) — Async Python API
- [ChromaDB](https://trychroma.com) — Vector memory
- [Framer Motion](https://framer.com/motion) — Animations

---

<div align="center">

**ARIA X — Built with ♥ for the future of human-AI interaction**

*"Intelligent. Empathetic. Always ready."*

</div>

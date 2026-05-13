# Hi, I'm Eugen 👋

**Procurement Professional transitioning into AI** | Berlin 🇩🇪

Currently attending the **AI Integration Bootcamp @ Ironhack Berlin** (Week 4 of 9) — building AI-powered tools that solve real operational problems.

---

## 🤖 Icarus AI — Personal Operating System (Live)

A JARVIS-style personal AI OS accessible via Telegram bot and a Progressive Web App 

| Capability | Detail |
|---|---|
| Natural language — text | Claude Sonnet 4.6 tool-use agent |
| Natural language — voice | OpenAI Whisper transcription |
| Image / document analysis | Claude multimodal — invoices, contracts, whiteboards |
| Google Calendar read | This week's events |
| Google Calendar write | Create, find, delete, recurring events |
| Gmail read | Important-only, last 3 days, time-based queries |
| Gmail search | Find any email by person, subject, folder, or date |
| Gmail full body | Read the actual message content |
| Email reply | Draft + Send / Edit / Cancel approval flow |
| Proactive email alerts | Polls every 15 min, AI urgency filter |
| Morning briefing | 06:00 Berlin — calendar + emails + tasks |
| Web search | Tavily API — live news, prices, company info |
| Google Maps | Places, directions, opening hours, ratings |
| GitHub Issues | Read open tasks, create new ones |
| Shopping list | Conversational, emoji categories, visual formatting, deduplicates |
| Expense tracker | Text or receipt photo, visual summary with store-type detection |
| LinkedIn posting | AI-drafted posts with Telegram approval flow |
| Hermes sub-agent | Monitors ~590 tech suppliers, generates market briefings and trend analysis |
| Persistent memory | Upstash Redis — survives restarts |
| Multi-model routing | Haiku for simple, Sonnet for complex (~€8-9/month) |

**Stack:** `Python` `FastAPI` `python-telegram-bot` `Claude Sonnet 4.6` `Claude Haiku 4.5` `OpenAI Whisper` `Google Calendar API` `Gmail API` `GitHub API` `Tavily API` `Google Maps API` `LinkedIn API` `Upstash Redis` `Railway` `GitHub Actions`

[→ View on GitHub](https://github.com/eugnmueller-87/Personal-Assistent) | [→ Project Kanban](https://github.com/users/eugnmueller-87/projects/6)

---

## 🔧 ICARUS Self-Healing System

ICARUS can diagnose and fix its own runtime errors without manual intervention.

**How it works:**

1. Any unhandled exception in a message handler is caught automatically
2. Extracts the traceback and identifies the failing source file
3. Claude Sonnet reads the broken file + full traceback and generates a corrected version
4. The fix is committed directly to the Railway-connected GitHub repo via the GitHub API
5. Railway detects the push and redeploys automatically (~90s)
6. On next startup, ICARUS checks a Redis flag and sends a Telegram report:
   *"Back online after auto-fix. Fixed: bot/claude_router.py: KeyError 'summary'"*
7. If the same file fails twice, it escalates: *"auto-fix exhausted — manual fix needed"*

**Stack:** `Claude Sonnet 4.6` `GitHub Contents API` `Upstash Redis` `Railway auto-deploy` `GitHub Actions`

[→ View on GitHub](https://github.com/eugnmueller-87/Personal-Assistent)

---

## 🔴 SpendLens — Procurement Intelligence Platform

An AI-powered procurement analytics platform built with Python and Panel.

- Uploads any spend dataset (CSV, Excel, SAP/Coupa exports) — messy columns auto-mapped via Claude AI
- Five-stage AI pipeline: column mapping → data cleanup → vendor classification → compliance flagging → supplier intelligence
- **Compliance Scorecard** — EcoVadis-style supplier cards with ABC tier classification, contract status, compliance scores
- **ICARUS** — embedded market intelligence agent monitoring RSS feeds, scoring articles, generating RFP & negotiation briefs
- CFO-ready Excel export with EBITDA impact reporting
- Persistent SQLite knowledge base — every upload appends to the timeline
- **n8n workflow automation** — procurement approval flows and process automation

**Stack:** `Python` `Panel` `Plotly` `Pandas` `Claude API` `SQLite` `Pydantic` `n8n`

---

## 🎙 PodcastIQ — Automated Podcast Studio (Ironhack Week 2 Capstone)

Converts PDFs, URLs, YouTube links, or plain text into polished two-host audio episodes in under 60 seconds.

- Multi-source ingestion: PDF, article URLs, YouTube transcripts, plain text
- 4 podcast styles: Educational, Debate, News Brief, Deep Dive
- Dual LLM: Claude Sonnet 4.6 (default) or GPT-4o
- Dual voice TTS: ElevenLabs (premium) + Microsoft edge-tts (fallback)
- 3-layer humanization: reactions, self-corrections, humor, emotional prosody
- Content safety: two-layer guard blocks harmful content
- Auto-generates episode metadata (title, summary, tags, listen time)
- Parallel async TTS synthesis — ~4s for a 20-line episode
- Estimated cost: ~$0.03–0.05 per episode

**Stack:** `Python 3.10+` `Gradio 6.x` `Claude Sonnet 4.6` `GPT-4o` `ElevenLabs` `edge-tts` `pydub` `ffmpeg` `PyPDF2` `BeautifulSoup4` `youtube-transcript-api`

[→ View on GitHub](https://github.com/eugnmueller-87/PODCAST-STUDIO)

---

## 🔍 Hermes — Market Intelligence Sub-Agent (Live)

A dedicated market intelligence service deployed on Railway, crawling ~590 tech/procurement suppliers across 17 categories. Hermes runs autonomously and answers Icarus AI's questions via a secured REST API.

**Architecture:** Icarus is master — Hermes is a pure data service. It never pushes alerts or touches personal data; it answers queries.

You (Telegram)
│
▼
ICARUS AI ──── HTTP (x-api-key) ──▶ HERMES AGENT
│
RSS / EDGAR / Tavily /
Jobs / Transcripts crawlers
│
Claude Haiku (11 signal types)
│
┌────────────────┴─────────────────┐
▼                                   ▼
Upstash Redis                      Upstash Vector
(items, profiles,                  (semantic RAG search,
clusters, TTLs)                    1024-dim BGE model)



**Crawlers (5 active, scheduled):**

| Crawler | Source | Schedule |
|---|---|---|
| RSS | ~590 company feeds + 18 industry feeds | Every 6 hours |
| EDGAR | SEC 8-K / 10-Q / 10-K filings (Tier 1+2) | Daily 07:30 |
| Tavily news | Deep web search, capped ~700/month | Monday 09:00 |
| Jobs | Lever / Greenhouse / Workday — hiring as forward indicator | Wednesday 09:00 |
| Earnings transcripts | SEC 8-K full text | Thursday 08:00 |

**Intelligence layer:**
- 11 signal types × HIGH/MEDIUM/LOW urgency — classified by Claude Haiku
- Company knowledge profiles in Redis — permanent, accumulate signal history + risk flags
- Macro theme clustering — Claude Sonnet groups cross-company signals into synthesis paragraphs (6h cache)
- Trend memory — weekly cluster snapshots with NEW / CONTINUING / RESOLVED delta
- Profile enrichment — auto-extracts key products, pricing notes, risk summaries at 10-signal threshold
- SpendLens connector — `HermesClient` with fuzzy vendor matching feeds signals directly into SpendLens

**Icarus has 8 tool calls mapped to Hermes:** `hermes_query` · `hermes_profile` · `hermes_briefing` · `hermes_search` · `hermes_trends` · `hermes_crawl` · `hermes_chart` · `hermes_greet`

**Stack:** `Python 3.13` `FastAPI` `APScheduler` `Claude Haiku 4.5` `Claude Sonnet 4.6` `Upstash Redis` `Upstash Vector (BGE 1024-dim)` `Tavily API` `EDGAR API` `QuickChart.io` `Railway` `GitHub Actions`

[→ View on GitHub](https://github.com/eugnmueller-87/hermes-agent)
Also update the Hermes sub-agent row in the Icarus capabilities table — change:

Monitors ~590 tech suppliers, generates market briefings and trend analysis

to:

Dedicated sub-agent — 5 crawlers, 590 suppliers, 11 signal types, RAG search, Claude Haiku classification

And remove the old AI Content Intelligence System section entirely, since that repo is spec-only and Hermes is the real thing.

---

## 🛠 Skills

**Procurement & Category Management**
Procurement, Category Management, Contract Negotiation, Purchase Management,
Team Leadership, Mentoring, Change Management, Strategic Planning,
Financial Analysis, Analytical Skills, Software as a Service (SaaS), Technology Trends

**AI & Engineering**
- Python · FastAPI · Pandas · Plotly · Panel · Gradio
- Anthropic Claude API · OpenAI API · Whisper STT · ElevenLabs TTS
- Multi-agent architecture · Tool-use agents · Multimodal AI · Sub-agent orchestration
- Telegram bot development · Progressive Web App (PWA) · Railway deployment
- Upstash Redis · SQLite · REST APIs · OAuth 2.0
- Git · GitHub Actions · CI/CD pipelines · pytest
- n8n workflow automation
- Security hardening: fail-closed auth · prompt injection defence · audit logging · auto-fix denylist
- Self-healing systems: exception capture · AI-generated fix · PR review gate · auto-redeploy
- LinkedIn Posts API · Little Text Format (LTF) · organisation @mentions

---

## 🏢 Background

| Company | Role |
|---------|------|
| TeamViewer | Lead Procurement & Category Management |
| Scout24 | Senior Procurement Manager |
| Delivery Hero / FoodPanda | Category Manager |

---

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Eugen%20Mueller-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/eugen-mueller)

---

*"Combining 10+ years of procurement expertise with AI engineering to build tools that actually solve real problems."*

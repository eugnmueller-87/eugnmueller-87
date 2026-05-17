# Hi, I'm Eugen 👋

**Procurement Leader → AI Engineer** | Berlin 🇩🇪

10+ years leading procurement and category management at **TeamViewer**, **Scout24**, and **Delivery Hero** — now engineering the AI systems that will transform the function I know inside out.

I don't just advise on AI transformation. I build the tools myself.

Every project here started with a real problem I personally encountered running procurement teams: manual triage, supplier compliance gaps, fragmented spend data, slow RFP cycles, and market intelligence that arrives too late. These are my answers — designed by someone who has lived them and built by someone who can now ship them.

Currently completing the **AI Integration Bootcamp @ Ironhack Berlin** (Week 5 of 9).

---

## Procurement AI Transformation

*AI-powered tools built from 10+ years of hands-on procurement experience — targeting the exact pain points category managers, CPOs, and procurement ops teams face daily.*

| Project/Description | GitHub |
|---|---|
| 🔴 **SpendLens** — Full-stack AI procurement intelligence platform. React 18 SPA served by FastAPI. Ingests any spend file (CSV, Excel, SAP/Coupa), auto-maps messy columns via Claude, runs a 5-stage pipeline: column mapping → data cleanup → vendor classification → compliance flagging → supplier intelligence. Dashboard with year-aware KPIs, YoY diverging bar chart, Category Risk Matrix, 5-year stacked area trend. Deep Dive with spend growth, treemap, drill-in category drawers. Compliance Scorecards (26 suppliers, ABC tiers, multi-filter). AI contract clause extraction with RiskArc gauge and renewal tracking (CLM). Category Strategy workbench — 7 AI frameworks (Kraljic, PESTEL, SWOT, Porter's, TCO, Negotiation Levers, + 10-slide HTML export. Icarus AI market signal feed with category tabs and Hermes integration. Deployed live on Railway. | [Link](https://github.com/eugnmueller-87/PROCUREMENT) |

| 🏗 **Autonomous Procurement Triage Agent** — End-to-end autonomous agent replacing manual PR triage. 5-tier routing by value (<€5k auto-approve → >€100k full RFP). Supplier NDA/DPA/MSA compliance check on every request via RAG. Guided business case builder for high-value purchases. RFQ/RFP document generation, multi-supplier outreach, quote collection, evaluation matrix, award recommendation. 6 importable n8n workflows. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB4) |
| 🔍 **Hermes — Market Intelligence Sub-Agent** — Autonomous sub-agent deployed on Railway. Crawls ~590 tech/procurement suppliers across 17 categories via 5 scheduled crawlers (RSS, EDGAR, Tavily, Jobs, Earnings transcripts). 11 signal types classified by Claude Haiku, semantic RAG search via Upstash Vector (1024-dim BGE), macro theme clustering, trend memory with NEW/CONTINUING/RESOLVED delta. Powers SpendLens and Icarus AI. | [Link](https://github.com/eugnmueller-87/hermes-agent) |
| ☠️ **Hades — Supplier Due Diligence Agent** — Production-deployed autonomous DD agent. POST a company name → full risk report in under 2 minutes. 6 parallel LangGraph nodes: OFAC SDN + UN SC sanctions (free XML, no key), NorthData company registry, BAFA/NCP/NGO LkSG/CSDDD compliance signals, ESG & labour risk, 90-day news sentiment, Hermes market intelligence. Claude Sonnet 4.6 synthesises into weighted risk score (1–10) + recommendation: Approve / Conditional Approval / Block. Auto-registers every supplier to Hermes watchlist for ongoing monitoring. | [Link](https://github.com/eugnmueller-87/hades) |

---

## Autonomous Agents & AI Systems

*Production multi-agent architectures, self-healing infrastructure, and real-time AI applications running live.*

| Project/Description | GitHub |
|---|---|
| 🤖 **Icarus AI — Personal Operating System** — JARVIS-style AI OS via Telegram + PWA. 20+ capabilities: voice input (Whisper), multimodal document analysis (invoices, contracts, whiteboards), Gmail/Calendar/GitHub integration, proactive email alerts, expense tracking, LinkedIn posting, live web search, Google Maps. Multi-model routing (Haiku for simple, Sonnet for complex). Persistent memory via Upstash Redis. ~€8–9/month. | [Link](https://github.com/eugnmueller-87/Personal-Assistent) |
| 🔧 **ICARUS Self-Healing System** — Icarus diagnoses and repairs its own runtime errors without human intervention. Catches exceptions → Claude reads broken file + traceback → generates corrected version → commits via GitHub API → Railway redeploys (~90s) → Telegram confirms fix. Escalates to manual review if the same file fails twice. | [Link](https://github.com/eugnmueller-87/Personal-Assistent) |

---

## Full-Stack AI Applications

*End-to-end products combining AI reasoning, workflow automation, and real-world integrations.*

| Project/Description | GitHub |
|---|---|
| 🏥 **Kita Connect** — Full-stack daycare management platform for German Kitas. ~€0/month operational cost, GDPR-compliant, Frankfurt-hosted. Three portals: parents (development docs, messaging, multi-language DE/EN/RU), educators (Sismik/Seldak/Perik observation tracking, AI-assisted learning stories via Claude Haiku), management (multi-channel comms — in-app, email, Telegram, SMS — automated registration workflows). | [Link](https://github.com/eugnmueller-87/kita-connect) |
| 🎙 **PodcastIQ — Automated Podcast Studio** — Any PDF, URL, YouTube link, or plain text → polished two-host MP3 episode in under 60 seconds. 4 podcast styles, dual LLM (Claude Sonnet / GPT-4o), ElevenLabs premium voices + edge-tts fallback, 3-layer humanizer, emotional prosody, content safety guard, parallel async TTS synthesis. ~$0.03–0.05 per episode. Ironhack Week 2 Capstone. | [Link](https://github.com/eugnmueller-87/PODCAST-STUDIO) |

---

## RAG Pipelines & Knowledge Systems

*Retrieval-augmented generation implementations — from basic chunking to advanced reranking and semantic search.*

| Project/Description | GitHub |
|---|---|
| 📚 **RAG Pipeline** — Chunking, embedding, retrieval with metadata filtering. Upstash Vector store, OpenAI embeddings, query pipeline with source tracking. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%202) |
| ⚖️ **Relevance Scoring & Rerankers** — Advanced RAG over EU AI Act legal text + podcast transcripts. Vector similarity retrieval, metadata filtering, Cohere cross-encoder reranking, LLM relevance scoring, before/after position-shift analysis. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%203/LAB%203) |
| 🔌 **MCP Integration** — LangChain tool-use agent connected to a local filesystem via Model Context Protocol. Demonstrates standardised tool discovery and direct-API comparison. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%203/LAB%204) |

---

## LangChain & LangGraph Agents

*Structured and unstructured agent workflows — from free tool selection to deterministic state machines.*

| Project/Description | GitHub |
|---|---|
| 🤖 **LangChain Tool-Use Agent** — ReAct-pattern agent with free tool selection across 4 custom tools. Agent decides which tools to call and in what order without a fixed script. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%202) |
| 🔄 **LangGraph Complaint Processor** — Deterministic 5-node state machine: intake → validate → investigate → resolve → close. Explicit edges, conditional transitions, human-in-the-loop checkpoints. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%203/LAB%204) |

---

## Workflow Automation (n8n)

*Production-ready n8n workflows for procurement, research, and operational automation.*

| Project/Description | GitHub |
|---|---|
| 🏗 **Procurement Triage Workflows** — 6 fully importable n8n workflows for the autonomous procurement agent: PR ingestion, tier routing & SMTP notifications, ERP integration (budget check + PO creation), RFQ/RFP supplier outreach with daily reminders, quote collection, approval response handling. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB4/n8n_workflows) |
| 📰 **arXiv Research Summarizer** — n8n + Claude + Notion pipeline. POST an arXiv URL → extract paper ID → fetch metadata via arXiv API → Claude summarises abstract → stores structured record in Notion research database. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/EXTRA%202) |
| ⚙️ **Error Handling & Scheduled Workflows** — n8n patterns for production resilience: HTTP retry logic (3×, 5s delay), error output branching, daily scheduled runs with idempotency guard via date-keyed IF node. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/EXTRA%203) |
| 🔍 **n8n Node Reference** — Systematic study of 20 node types across 3 workflows. Parameters, JSON input/output, key transformations, debugging tips. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB2) |

---

## 🛠 Skills

**Procurement & AI Transformation**
Procurement Strategy · Category Management · Contract Negotiation · Supplier Management · Source-to-Pay (S2P) · RFQ/RFP Design · Supplier Evaluation · Spend Analytics · GDPR Compliance · Change Management · AI Process Automation · Autonomous Agent Design · n8n Workflow Automation · ERP Integration (SAP/Coupa)

**Engineering**
`Python` `FastAPI` `Next.js` `LangChain` `LangGraph` `RAG` `ChromaDB` `Upstash Redis & Vector`
`Claude API` `OpenAI API` `Whisper` `ElevenLabs` `n8n` `Gradio` `Panel` `Plotly` `Pandas`
`Supabase` `SQLite` `REST APIs` `OAuth 2.0` `Telegram Bot API` `Railway` `Vercel`
`GitHub Actions` `CI/CD` `Multi-agent orchestration` `Self-healing systems`

---

## 🏢 Background

| Company | Role |
|---|---|
| TeamViewer | Lead Procurement & Category Management |
| Scout24 | Senior Procurement Manager |
| Delivery Hero / FoodPanda | Category Manager |

---

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Eugen%20Mueller-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/eugen-mueller)

---

*10+ years of procurement expertise. Now building the AI systems that will transform how procurement teams operate.*

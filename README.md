# Hi, I'm Eugen 👋

**Procurement Leader → AI Engineer** | Berlin 🇩🇪

10+ years leading procurement and category management at **TeamViewer**, **Scout24**, **Foodpanda** and **Delivery Hero** — now engineering the AI systems that will transform the function I know inside out.

I don't just advise on AI transformation. I build the tools myself.

Every project here started with a real problem I personally encountered running procurement teams: manual triage, supplier compliance gaps, fragmented spend data, slow RFP cycles, and market intelligence that arrives too late. These are my answers — designed by someone who has lived them and built by someone who can now ship them.

Completed **AI Integration Bootcamp @ Ironhack Berlin**. Now in production.

---

## Procurement AI Transformation

*AI-powered tools built from 10+ years of hands-on procurement experience — targeting the exact pain points category managers, CPOs, and procurement ops teams face daily.*

| Project | Description | GitHub |
|---|---|---|
| 🧠 **TrueSpend** | AI-native procurement OS. n8n + Claude Sonnet 4.6 + PostgreSQL + React. 12 autonomous workflows, 28-table schema, Operations Board with full P2I lifecycle, 4-agent compliance onboarding, DocuSign e-signature (JWT Grant, embedded signing), Grafana observability, Jira for ≥€100k escalations. 41 live mock tickets. Deployed on Railway. | [Link](https://github.com/eugnmueller-87/TrueSpend) |
| 🔴 **SpendLens** | Full-stack AI procurement intelligence platform. React 18 SPA + FastAPI. 5-stage AI pipeline: column mapping → cleanup → vendor classification → compliance flagging → supplier intelligence. 7 screens: Dashboard, Deep Dive, Compliance Scorecard, CLM, Icarus AI, Supplier DD, Category Strategy. Deployed live on Railway. | [Link](https://github.com/eugnmueller-87/PROCUREMENT) |
| 🏗 **Triage Agent** | Autonomous agent replacing manual PR triage. 5-tier value routing, supplier NDA/DPA/MSA compliance check via RAG, RFQ/RFP generation, multi-supplier outreach, evaluation matrix, award recommendation. 6 importable n8n workflows. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB4) |
| 🔍 **Hermes** | Market intelligence sub-agent on Railway. Crawls 590+ suppliers across 17 categories via 5 crawlers (RSS, EDGAR, Tavily, Jobs, Earnings). Signals classified by Claude Haiku with delta tracking. Semantic RAG via Upstash Vector. Powers SpendLens Icarus AI. | [Link](https://github.com/eugnmueller-87/hermes-agent) |
| ☠️ **Hades** | Supplier due diligence agent. POST a company name, get a full risk report in under 2 minutes. 6 parallel LangGraph nodes: OFAC/UN sanctions, NorthData registry, LkSG/CSDDD signals, ESG, news sentiment, Hermes intel. Risk score 1–10 + Approve/Block recommendation. Integrated into SpendLens. | [Link](https://github.com/eugnmueller-87/hades) |
| 📊 **Marketing Channel Statistical Analysis** | Full statistical pipeline for $500K marketing budget allocation across 7 channels. 90-day dataset, Welch t-tests + Fisher's exact test, Bonferroni + Benjamini-Hochberg FDR correction, empirical power analysis (1,000 simulations), bootstrap confidence intervals, Cohen's d effect sizes. All 14 CPA pairs and 21 conversion rate pairs significant post-FDR. Executive memo with data-backed reallocation recommendation. Ironhack Week 6 Lab. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/Week%206/LAB%209/lab_statistical_analysis_eugen_mueller) |
| 🧪 **Rating System for AI Responses** | LLM evaluation framework for procurement compliance Q&A. Custom 20-example dataset (risk, compliance, data-privacy, contractual, financial). LLM-as-judge evaluators for correctness + completeness. A/B model comparison: gpt-4o-mini vs gpt-4o. Built with LangSmith, openevals, and OpenAI. Ironhack Week 6 Lab. | [Link](https://github.com/eugnmueller-87/Rating-System-for-AI-Responses) |

---

## Autonomous Agents & AI Systems

*Production multi-agent architectures, self-healing infrastructure, and real-time AI applications running live.*

| Project/Description | GitHub |
|---|---|
| 🤖 **Icarus AI — Personal Operating System** — JARVIS-style AI OS via Telegram + PWA. 20+ capabilities: voice input (Whisper), multimodal document analysis (invoices, contracts, whiteboards), Gmail/Calendar/GitHub integration, proactive email alerts, expense tracking, LinkedIn posting, live web search, Google Maps. Multi-model routing (Haiku for simple, Sonnet for complex). Persistent memory via Upstash Redis. ~€8–9/month. | [Link](https://github.com/eugnmueller-87/Personal-Assistent) |
| 🔧 **ICARUS Self-Healing System** — Icarus diagnoses and repairs its own runtime errors without human intervention. Catches exceptions → Claude reads broken file + traceback → generates corrected version → commits via GitHub API → Railway redeploys (~90s) → Telegram confirms fix. Escalates to manual review if the same file fails twice. | [Link](https://github.com/eugnmueller-87/Personal-Assistent) |
| ⚡ **Pantheon OS — Autonomous Trading Orchestrator** — 8-agent trading system. **Live on Hetzner. Paper trading. Self-scheduling every 15 minutes.** ZEUS orchestrates: **Icarus** (Hermes signal watcher, 590+ suppliers) → **Hades** (OFAC/EU sanctions/ESG compliance firewall) → **Artemis** (VIX + macro regime) → **Pythia** (Kelly-inspired sizing from historical win rates) → **Zeus** (Claude Sonnet 4.6 LLM reasoning + ChromaDB KB + ticker history) → **Ares** (IBKR bracket orders: entry + 3% SL + 6% TP) → **Argus** (drawdown kill switch + portfolio monitor). **Apollo** runs daily: arXiv ingestion, earnings enrichment, self-improvement loop. Agent seniority system gates live trading — agents level up from TRAINEE → DIRECTOR as they build verified win rates. Grafana dashboard tracks equity, drawdown, agent health, and Anthropic token spend. Kafka event bus. Supabase persistence. | [Link](https://github.com/eugnmueller-87/Pantheon) |

---

## Client Work

*Production AI systems built for paying clients — real problems, live infrastructure.*

| Project/Description | GitHub |
|---|---|
| 📊 **Client Dashboard** — Internal agency dashboard for monitoring all live client AI systems in one place. Real-time status, deployment health, and pipeline metrics across projects. | [Link](https://github.com/eugnmueller-87/CLIENT-DASHBOARD) |
| 🧙 **Agency Wizard** — Internal onboarding wizard for deploying full AI automation stacks to clients in a single 3-hour session. Validates every credential live, then provisions everything directly into the client's own n8n Cloud instance. Password-protected, branded per client. | [Link](https://github.com/eugnmueller-87/Agency-Wizard) |
| 🩺 **AI Triage System** — Autonomous customer support triage for a Croatian gut health brand (Metabelly). Incoming emails classified by AI agent (category, priority, language), auto-replies drafted for FAQ and medical deflections, Calendly booking links appended, results routed to Slack. Built on n8n + Mistral AI + Gmail API. GDPR-compliant: no PII in summaries, content processed in memory only. | [Link](https://github.com/eugnmueller-87/Metabelly) |
| 📧 **Noosphr Workspace — Email Router** — AI-powered email triage for Noosphr's company inbox. Incoming emails classified by Claude AI (Haiku) and routed to `#business`, `#support`, or `#spam` Slack channels with one-click reply buttons. Runs as a systemd service on a Hetzner VPS. Hostinger IMAP + Slack Incoming Webhooks + Anthropic API. | [Link](https://github.com/eugnmueller-87/Noosphr-Workspace) |

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
| 🧠 **TrueSpend Workflows (12)** — intake_receiver, docusign_sign, supplier_reply_handler, contract_watcher, reorder_trigger, hyperscaler_monitor, supplier_onboarding, invoice_processor, delivery_confirmation, asset_depreciation, llm_consumption, docusign_received. All production-grade: 120s timeouts, 3× retry, full trace logging per signal. DocuSign JWT Grant with embedded signing. | [Link](https://github.com/eugnmueller-87/TrueSpend/tree/main/workflows) |
| 🏗 **Procurement Triage Workflows** — 6 fully importable n8n workflows for the autonomous procurement agent: PR ingestion, tier routing & SMTP notifications, ERP integration (budget check + PO creation), RFQ/RFP supplier outreach with daily reminders, quote collection, approval response handling. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB4/n8n_workflows) |
| 📰 **arXiv Research Summarizer** — n8n + Claude + Notion pipeline. POST an arXiv URL → extract paper ID → fetch metadata via arXiv API → Claude summarises abstract → stores structured record in Notion research database. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/EXTRA%202) |
| ⚙️ **Error Handling & Scheduled Workflows** — n8n patterns for production resilience: HTTP retry logic (3×, 5s delay), error output branching, daily scheduled runs with idempotency guard via date-keyed IF node. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/EXTRA%203) |
| 🔍 **n8n Node Reference** — Systematic study of 20 node types across 3 workflows. Parameters, JSON input/output, key transformations, debugging tips. | [Link](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB2) |

---

## 🛠 Skills

**Procurement & AI Transformation**

![Procurement Strategy](https://img.shields.io/badge/Procurement%20Strategy-0A66C2?style=flat)
![Category Management](https://img.shields.io/badge/Category%20Management-0A66C2?style=flat)
![Contract Negotiation](https://img.shields.io/badge/Contract%20Negotiation-0A66C2?style=flat)
![Supplier Management](https://img.shields.io/badge/Supplier%20Management-0A66C2?style=flat)
![Source-to-Pay](https://img.shields.io/badge/Source--to--Pay%20%28S2P%29-0A66C2?style=flat)
![RFQ/RFP Design](https://img.shields.io/badge/RFQ%2FRFP%20Design-0A66C2?style=flat)
![Supplier Evaluation](https://img.shields.io/badge/Supplier%20Evaluation-0A66C2?style=flat)
![Spend Analytics](https://img.shields.io/badge/Spend%20Analytics-0A66C2?style=flat)
![GDPR Compliance](https://img.shields.io/badge/GDPR%20Compliance-0A66C2?style=flat)
![Change Management](https://img.shields.io/badge/Change%20Management-0A66C2?style=flat)
![AI Process Automation](https://img.shields.io/badge/AI%20Process%20Automation-0A66C2?style=flat)
![Autonomous Agent Design](https://img.shields.io/badge/Autonomous%20Agent%20Design-0A66C2?style=flat)
![n8n Workflow Automation](https://img.shields.io/badge/n8n%20Workflow%20Automation-0A66C2?style=flat)
![ERP Integration](https://img.shields.io/badge/ERP%20Integration%20%28SAP%2FCoupa%29-0A66C2?style=flat)
![Statistical Analysis](https://img.shields.io/badge/Statistical%20Analysis-0A66C2?style=flat)

**Engineering**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat&logo=tailwindcss&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![PostgREST](https://img.shields.io/badge/PostgREST-4169E1?style=flat)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-FF6B35?style=flat)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=flat)
![Upstash Redis](https://img.shields.io/badge/Upstash%20Redis%20%26%20Vector-00C896?style=flat&logo=redis&logoColor=white)
![Claude API](https://img.shields.io/badge/Claude%20API-CC785C?style=flat)
![OpenAI API](https://img.shields.io/badge/OpenAI%20API-412991?style=flat&logo=openai&logoColor=white)
![Whisper](https://img.shields.io/badge/Whisper-412991?style=flat&logo=openai&logoColor=white)
![ElevenLabs](https://img.shields.io/badge/ElevenLabs-000000?style=flat)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-F97316?style=flat)
![Panel](https://img.shields.io/badge/Panel-4B8BBE?style=flat)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![REST APIs](https://img.shields.io/badge/REST%20APIs-FF6B35?style=flat)
![OAuth 2.0](https://img.shields.io/badge/OAuth%202.0-4A90D9?style=flat)
![DocuSign](https://img.shields.io/badge/DocuSign%20eSignature-FFB600?style=flat&logo=docusign&logoColor=black)
![Telegram Bot API](https://img.shields.io/badge/Telegram%20Bot%20API-26A5E4?style=flat&logo=telegram&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat&logo=railway&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![CI/CD](https://img.shields.io/badge/CI%2FCD-2088FF?style=flat&logo=githubactions&logoColor=white)
![Multi-agent Orchestration](https://img.shields.io/badge/Multi--agent%20Orchestration-8B5CF6?style=flat)
![Self-healing Systems](https://img.shields.io/badge/Self--healing%20Systems-8B5CF6?style=flat)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Hetzner](https://img.shields.io/badge/Hetzner-D50C2D?style=flat&logo=hetzner&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat&logo=nginx&logoColor=white)
![IB Gateway](https://img.shields.io/badge/IB%20Gateway-CC0000?style=flat)
![ib_insync](https://img.shields.io/badge/ib__insync-CC0000?style=flat)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![Interactive Brokers](https://img.shields.io/badge/Interactive%20Brokers-CC0000?style=flat)

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

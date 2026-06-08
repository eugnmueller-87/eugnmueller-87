# Hi, I'm Eugen 👋

**Procurement Leader → AI Engineer** | Berlin 🇩🇪

10+ years leading procurement and category management at **TeamViewer**, **Scout24**, **Foodpanda** and **Delivery Hero** — now engineering the AI systems that will transform the function I know inside out.

I don't just advise on AI transformation. I build the tools myself.

Every project here started from a real problem I encountered running procurement teams: manual triage, supplier compliance gaps, fragmented spend data, slow RFP cycles, and market intelligence that arrives too late. These are my answers — designed by someone who has lived them and built by someone who can now ship them.

Completed **AI Integration Bootcamp @ Ironhack + MBA-IT. Now in production.

---

## Procurement AI Transformation

*AI-powered tools built from 10+ years of hands-on procurement experience — targeting the exact pain points category managers, CPOs, and procurement ops teams face daily.*

| Project | Description | Links |
|---|---|---|
| 🧠 **TrueSpend** | AI-native procurement OS. n8n + Claude Sonnet 4.6 + PostgreSQL + React. 14 autonomous workflows, 28-table schema, full P2I lifecycle. Role-gated Operations Board (procurement, IT, controlling, legal, admin). 4-agent compliance onboarding, DocuSign JWT Grant, Grafana, Jira ≥€100k. DB-enforced security: NOSUPERUSER PostgREST role, all status transitions through SECURITY DEFINER RPCs — `PATCH tickets.status` → 403 at the database layer. | [GitHub](https://github.com/eugnmueller-87/TrueSpend) · [Live Demo](https://intake-production-84a0.up.railway.app) |
| 🔴 **SpendLens** | Full-stack AI procurement intelligence platform. React 18 SPA + FastAPI. 5-stage AI pipeline: column mapping → cleanup → vendor classification → compliance flagging → supplier intelligence. 7 screens: Dashboard, Deep Dive, Compliance Scorecard, CLM, Icarus AI, Supplier DD, Category Strategy. | [GitHub](https://github.com/eugnmueller-87/PROCUREMENT) |
| 🏗 **Triage Agent** | Autonomous agent replacing manual PR triage. 5-tier value routing, supplier NDA/DPA/MSA compliance check via RAG, RFQ/RFP generation, multi-supplier outreach, evaluation matrix, award recommendation. 6 importable n8n workflows. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB4) |
| 📦 **SCM-Master** | AI-native supply-chain OS unifying procurement, transit-warehouse flow, and full asset lifecycle. FastAPI + SQLAlchemy 2.0 + Pydantic 2 (SQLite→Postgres), JWT role-gating, **273 tests**, 6-job CI (lint · Postgres · SAST · CVE-audit · agent-safety). Multi-sourcing core: `Product` decoupled from `ProductSupplier` (lead time, MOQ, price, rank) — re-sourcing a line is one FK repoint. Serial-tracked `Asset` traced end-to-end (RECEIVED → … → DISPOSED) with an unbroken provenance link to its PO line. Contract lifecycle + budget burn, capacity with one-click rebalance, and an autonomous **weekly purchasing run** (demand-justified, one-PO-per-supplier, approve→place) under the rule **"the LLM advises, deterministic code decides"** — proven by a **29-scenario agent-safety harness** that feeds the gate hostile AI advice (unapproved supplier, over-cap spend, prompt injection, poisoned calibration) and asserts it refuses, every time. **Real inventory science:** a **Syntetos–Boylan** classifier routes each SKU's demand to the right forecaster (run-rate vs **TSB** for lumpy), with the **walk-forward backtest as the arbiter** (run-rate wins → stays default; the honest finding that lumpy demand is absorbed by stock, not forecasts); **service-level safety stock** (`z × σ` over lead-time buckets) + **ABC** per-class service levels. **Deployed as two fully-isolated stacks** (separate Railway projects + Postgres) — a self-wiring public demo and a **forge-locked production** (refuses to seed, ship demo accounts, or run on non-persistent storage; the weak-admin refusal is regression-tested); each with its own [analytics cockpit](https://github.com/eugnmueller-87/SCM-POWER-BI). **Cost-intelligence layer:** a clean-sheet **should-cost engine** (components indexed to commodity markets → a defensible cost floor + target price, so you negotiate from *our* number, with DRAM/NAND sensitivity), and full per-asset **TCO** (acquisition + landed + deployment + lifetime OpEx + EOL − recovery) rolling up to a correctly-defined **TSCMC %** — deterministic engines, the LLM only proposes. | [GitHub](https://github.com/eugnmueller-87/SCM-Master) · [Live Demo](https://scm-master-production.up.railway.app) |
| 📈 **SCM Power BI Cockpit** | AI-adoption **consulting case** for a non-technical CEO: *should a cloud/hosting enterprise invest in AI demand forecasting?* Synthetic-data generator → 7 internally-consistent CSVs feed a **live, auto-refreshing 7-tab web cockpit** (Node + Chart.js — Overview, SC Scorecard, Spend, Inventory, Forecast, **Should-Cost** margin-lever, **TCO**; cross-filter, click-to-drill KPIs, dynamic reorder alerts, forecast why-it-missed/how-to-fix diagnostics) **and** a Power BI report on the same live API — DAX measures anchored to **SCOR DS**, forecast accuracy (WMAPE / Bias / RMSE), should-cost & TCO. Backed by **cited market research** (Stanford AI Index, McKinsey, chip-geopolitics) and a **hype-vs-evidence** analysis driving an **invest / wait / pilot** recommendation, with a phased implementation plan + cost/timeline. | [GitHub](https://github.com/eugnmueller-87/SCM-POWER-BI) · [Live Dashboard](https://scm-power-bi-production.up.railway.app/) |
| 🔍 **Hermes** | Market intelligence sub-agent. Crawls 590+ suppliers across 17 categories via 5 crawlers (RSS, EDGAR, Tavily, Jobs, Earnings). Signals classified by Claude Haiku with delta tracking. Semantic RAG via Upstash Vector. Powers SpendLens Icarus AI. | [GitHub](https://github.com/eugnmueller-87/hermes-agent) |
| ☠️ **Hades** | Supplier due diligence agent. POST a company name, get a full risk report in under 2 minutes. 6 parallel LangGraph nodes: OFAC/UN sanctions, NorthData registry, LkSG/CSDDD signals, ESG, news sentiment, Hermes intel. Risk score 1–10 + Approve/Block recommendation. | [GitHub](https://github.com/eugnmueller-87/hades) |
| 📊 **Marketing Channel Statistical Analysis** | Full statistical pipeline for $500K marketing budget allocation across 7 channels. Welch t-tests, Bonferroni + BH-FDR correction, bootstrap CIs, Cohen's d. All 14 CPA pairs significant post-FDR. Executive memo with data-backed reallocation. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/Week%206/LAB%209/lab_statistical_analysis_eugen_mueller) |
| 🧪 **LLM Evaluation Framework** | LangSmith evaluation lab for procurement compliance Q&A. Custom 20-example dataset, LLM-as-judge correctness + completeness evaluators, A/B model comparison (gpt-4o-mini vs gpt-4o). | [GitHub](https://github.com/eugnmueller-87/Rating-System-for-AI-Responses) |

---

## Autonomous Agents & AI Systems

*Production multi-agent architectures, self-healing infrastructure, and real-time AI applications running live.*

| Project/Description | GitHub |
|---|---|
| ⚡ **Pantheon OS — Autonomous Trading Orchestrator** — 8-agent system live on Hetzner, self-scheduling every 15 minutes. **ZEUS** orchestrates: **Icarus** (Hermes signal watcher) → **Hades** (OFAC/EU sanctions firewall) → **Artemis** (VIX + macro regime) → **Pythia** (Kelly-inspired position sizing) → **Zeus** (Claude Sonnet 4.6 reasoning + ChromaDB KB) → **Ares** (IBKR bracket orders: entry + 3% SL + 6% TP) → **Argus** (drawdown kill switch). **Apollo** runs daily: arXiv ingestion, earnings enrichment, self-improvement loop. Agent seniority system: TRAINEE → DIRECTOR, gated by verified win rate. Kafka event bus. Supabase + Grafana. | [GitHub](https://github.com/eugnmueller-87/Pantheon) |
| 🤖 **Icarus AI — Personal Operating System** — JARVIS-style AI OS via Telegram + PWA. 20+ capabilities: voice input (Whisper), multimodal document analysis, Gmail/Calendar/GitHub integration, proactive alerts, expense tracking, LinkedIn posting, live web search. Multi-model routing. Persistent memory via Upstash Redis. ~€8–9/month. | [GitHub](https://github.com/eugnmueller-87/Personal-Assistent) |
| 🔧 **ICARUS Self-Healing System** — Icarus diagnoses and repairs its own runtime errors. Catches exceptions → Claude reads broken file + traceback → generates corrected version → commits via GitHub API → Railway redeploys (~90s) → Telegram confirms fix. Escalates if same file fails twice. | [GitHub](https://github.com/eugnmueller-87/Personal-Assistent) |

---

## Infrastructure & Security

*Self-hosted reliability and security tooling that keeps the production stack healthy — observe-only guardians, firewall hardening, and automated secret hygiene.*

| Project/Description | Repo |
|---|---|
| 🛡 **Lookout — Docker Host Guardian** — Observe-only watchdog for the production Docker hosts. Samples every container's CPU + memory each minute; on a sustained runaway it applies a reversible CPU cap (the only automatic action) and alerts via Telegram, leaving pause/restart/kill as owner-gated commands. Plus: firewall hardening (ufw + DOCKER-USER conntrack rules that actually block Docker-published ports), short-lived auto-rotated service tokens (no long-lived credentials on disk), a repo secret-scanner that watches all public repos for exposed keys, and a push-based health feed so the ops assistant can answer "are the servers running well?" in natural language. | [Private repo](https://github.com/eugnmueller-87/Lookout) |

## Client Work

*Production AI systems built for paying clients.*

| Project/Description | GitHub |
|---|---|
| 📊 **Client Dashboard** — Internal agency dashboard for monitoring all live client AI systems. Real-time status, deployment health, pipeline metrics across projects. | [GitHub](https://github.com/eugnmueller-87/CLIENT-DASHBOARD) |
| 🧙 **Agency Wizard** — Internal onboarding wizard for deploying full AI automation stacks to clients in a single 3-hour session. Validates every credential live, then provisions into the client's own n8n Cloud instance. | [GitHub](https://github.com/eugnmueller-87/Agency-Wizard) |
| 🩺 **AI Triage System (Metabelly)** — Autonomous customer support triage for a Croatian gut health brand. Incoming emails classified by AI (category, priority, language), auto-replies drafted, Calendly links appended, results routed to Slack. n8n + Mistral AI + Gmail API. GDPR-compliant. | [GitHub](https://github.com/eugnmueller-87/Metabelly) |
| 📧 **Noosphr Email Router** — AI email triage for Noosphr's inbox. Claude Haiku classifies and routes to `#business`, `#support`, or `#spam` Slack channels with one-click reply buttons. Runs as systemd service on Hetzner VPS. | [GitHub](https://github.com/eugnmueller-87/Noosphr-Workspace) |

---

## Full-Stack AI Applications

| Project/Description | GitHub |
|---|---|
| 🏥 **Kita Connect** — Full-stack daycare management platform for German Kitas. ~€0/month, GDPR-compliant, Frankfurt-hosted. Three portals: parents, educators (AI-assisted learning stories via Claude Haiku), management (multi-channel comms, automated registrations). | [GitHub](https://github.com/eugnmueller-87/kita-connect) |
| ⚡ **Light-weight Transcriber** — Drop a YouTube URL or paste any text. Ask Claude anything about it. Instant answers, no audio download, no fluff. Faster than anything comparable. | [GitHub](https://github.com/eugnmueller-87/Light-weight-Transcriber) |

---

## RAG, LangChain & LangGraph

| Project/Description | GitHub |
|---|---|
| 📚 **RAG Pipeline** — Chunking, embedding, retrieval with metadata filtering. Upstash Vector, OpenAI embeddings, query pipeline with source tracking. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%202) |
| ⚖️ **Relevance Scoring & Rerankers** — Advanced RAG over EU AI Act legal text. Vector similarity, metadata filtering, Cohere cross-encoder reranking, before/after position-shift analysis. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%203/LAB%203) |
| 🤖 **LangChain Tool-Use Agent** — ReAct-pattern agent with free tool selection across 4 custom tools. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%202) |
| 🔄 **LangGraph Complaint Processor** — Deterministic 5-node state machine with human-in-the-loop checkpoints. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%203/LAB%204) |

---

## Workflow Automation (n8n)

| Project/Description | GitHub |
|---|---|
| 🧠 **TrueSpend Workflows (12)** — intake_receiver, docusign_sign, supplier_reply_handler, contract_watcher, reorder_trigger, hyperscaler_monitor, supplier_onboarding, invoice_processor, delivery_confirmation, asset_depreciation, llm_consumption, docusign_received. Production-grade: 120s timeouts, 3× retry, per-signal trace logging. Status transitions call SECURITY DEFINER RPCs — no workflow writes `tickets.status` directly. | [GitHub](https://github.com/eugnmueller-87/TrueSpend/tree/main/workflows) |
| 🏗 **Procurement Triage Workflows** — 6 importable n8n workflows: PR ingestion, tier routing, ERP budget/PO, RFQ/RFP outreach, quote collection, approval handling. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB4/n8n_workflows) |
| 📰 **arXiv Research Summarizer** — n8n + Claude + Notion. POST an arXiv URL → fetch metadata → Claude summary → Notion record. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/EXTRA%202) |

---

## 🛠 Skills

**Procurement & Strategy**

![Procurement Strategy](https://img.shields.io/badge/Procurement%20Strategy-0A66C2?style=flat)
![Category Management](https://img.shields.io/badge/Category%20Management-0A66C2?style=flat)
![Contract Negotiation](https://img.shields.io/badge/Contract%20Negotiation-0A66C2?style=flat)
![Supplier Management](https://img.shields.io/badge/Supplier%20Management-0A66C2?style=flat)
![Source-to-Pay](https://img.shields.io/badge/Source--to--Pay%20%28S2P%29-0A66C2?style=flat)
![Spend Analytics](https://img.shields.io/badge/Spend%20Analytics-0A66C2?style=flat)
![GDPR Compliance](https://img.shields.io/badge/GDPR%20Compliance-0A66C2?style=flat)
![AI Process Automation](https://img.shields.io/badge/AI%20Process%20Automation-0A66C2?style=flat)
![Autonomous Agent Design](https://img.shields.io/badge/Autonomous%20Agent%20Design-0A66C2?style=flat)
![ERP Integration](https://img.shields.io/badge/ERP%20Integration%20%28SAP%2FCoupa%29-0A66C2?style=flat)

**Engineering**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white)
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
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white)
![DocuSign](https://img.shields.io/badge/DocuSign%20eSignature-FFB600?style=flat&logo=docusign&logoColor=black)
![Telegram Bot API](https://img.shields.io/badge/Telegram%20Bot%20API-26A5E4?style=flat&logo=telegram&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat&logo=railway&logoColor=white)
![Hetzner](https://img.shields.io/badge/Hetzner-D50C2D?style=flat&logo=hetzner&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Interactive Brokers](https://img.shields.io/badge/Interactive%20Brokers-CC0000?style=flat)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat&logo=nginx&logoColor=white)

**Data & BI**

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)
![Data Visualization](https://img.shields.io/badge/Data%20Visualization-8B5CF6?style=flat)
![BI Dashboards](https://img.shields.io/badge/BI%20Dashboards-8B5CF6?style=flat)
![Demand Forecasting](https://img.shields.io/badge/Demand%20Forecasting-8B5CF6?style=flat)
![Should-Cost / TCO](https://img.shields.io/badge/Should--Cost%20%2F%20TCO-8B5CF6?style=flat)

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

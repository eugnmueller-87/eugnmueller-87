

**AI Solutions Consultant for Procurement** | Berlin 🇩🇪

10+ years leading procurement and category management at **TeamViewer**, **Scout24**, **Foodpanda** and **Delivery Hero** — now engineering the AI systems that will transform the function I know inside out.

I don't just advise on AI transformation. I build the tools myself.

Every project here started from a real problem I encountered running procurement teams: manual triage, supplier compliance gaps, fragmented spend data, slow RFP cycles, and market intelligence that arrives too late. These are my answers — designed by someone who has lived them and built by someone who can now ship them.

AI Integration Bootcamp @ Ironhack · MBA-IT. I ship the tools, not just the slides, every project below is live and demoable.

<p align="center">
  <img src="screenshot/procurement-ai-transformation-banner.png" alt="From manual, paper-bound procurement to an AI-automated, autonomous function — the transformation I build" width="100%">
</p>

---

## Procurement AI Transformation

*AI-powered tools built from 10+ years of hands-on procurement experience — targeting the exact pain points category managers, CPOs, and procurement ops teams face daily.*

| Project | Description | Links |
|---|---|---|
| 🧠 **AI-native procurement OS** |TrueSpend. n8n + Claude Sonnet 4.6 + PostgreSQL + React. 17 autonomous workflows, 32-table schema (dbmate-migrated), full P2I lifecycle. Role-gated Operations Board (procurement, IT, controlling, legal, admin). 4-agent compliance onboarding, DocuSign JWT Grant, Grafana, Jira ≥€100k. **DB-enforced security:** NOSUPERUSER PostgREST role, every status transition through SECURITY DEFINER RPCs — `PATCH tickets.status` → 403 at the database layer. **Agent security:** inbound email/invoices run under "the LLM advises, deterministic code decides" — model output is schema-validated against an action allowlist, ticket/PO ids are derived deterministically (never from the model), and a prompt-injection repro proves the guard inert; money RPCs gated fail-closed off the browser token. | [GitHub](https://github.com/eugnmueller-87/TrueSpend) · [Live Demo](https://intake-production-84a0.up.railway.app) |
| 🔴 **Full-stack AI procurement intelligence platform** | SpendLens. React 18 SPA + FastAPI. 5-stage AI pipeline: column mapping → cleanup → vendor classification → compliance flagging → supplier intelligence, persisted to per-client SQLite (immutable raw layer, hash-dedup, recomputable enrichment). 7 screens: Dashboard, Deep Dive, Compliance Scorecard, CLM, Icarus AI, Supplier DD, Category Strategy — wired to **Hades** (supplier due-diligence) and **Hermes** (market intelligence). **Security-hardened for public deployment:** opt-in shared-secret API auth (constant-time compare, docs disabled in prod), scoped CORS + full security-header/CSP middleware, chunked upload guards (type allowlist + 25 MB cap), per-IP rate limiting on Anthropic-billed endpoints, Pydantic-validated Hades proxy (SSRF surface closed), and generic client errors with server-side logging — no exception leakage. **Production-polished frontend:** React production builds + SRI, pre-paint theme (no dark-mode flash), keyboard-accessible shell (focus-visible, ARIA roles), reduced-motion support, and an error boundary that keeps the shell alive on screen crashes. | [GitHub](https://github.com/eugnmueller-87/PROCUREMENT) · [Live Demo](https://procurement-production-f940.up.railway.app) |
| 🏗 **Triage Agent** | Autonomous agent replacing manual PR triage. 5-tier value routing, supplier NDA/DPA/MSA compliance check via RAG, RFQ/RFP generation, multi-supplier outreach, evaluation matrix, award recommendation. 6 importable n8n workflows. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB4) |
| 📦 **AI-native supply-chain OS** | SCM MASTER, AI-native supply-chain OS unifying procurement, transit-warehouse flow, and full asset lifecycle. FastAPI + SQLAlchemy 2.0 + Pydantic 2 (SQLite→Postgres), JWT role-gating, **52 test files · CI-gated ≥80% coverage**, 5-job CI (lint · Postgres · SAST · CVE-audit · agent-safety). Multi-sourcing core: `Product` decoupled from `ProductSupplier` (lead time, MOQ, price, rank) — re-sourcing a line is one FK repoint. Serial-tracked `Asset` traced end-to-end (RECEIVED → … → DISPOSED) with an unbroken provenance link to its PO line. Contract lifecycle + budget burn, capacity with one-click rebalance, and an autonomous **weekly purchasing run** (demand-justified, one-PO-per-supplier, approve→place) under the rule **"the LLM advises, deterministic code decides"** — the **confidence score is itself deterministic and audited** (factor-by-factor), gating auto-place at **≥0.90 confidence & <€200k** — proven by a **29-scenario agent-safety harness** that feeds the gate hostile AI advice (unapproved supplier, over-cap spend, prompt injection, poisoned calibration) and asserts it refuses, every time. **Real inventory science:** a **Syntetos–Boylan** classifier routes each SKU's demand to the right forecaster (run-rate vs intermittent), now backed by **Nixtla `statsforecast`** (Croston/SBA) with **conformal prediction-interval safety stock** — chosen over a hand-rolled TSB on a walk-forward benchmark (the honest finding: lumpy demand is absorbed by stock, not forecasts); **service-level safety stock** (`z × σ` over lead-time buckets) + **ABC** per-class service levels. **Learning layer:** rule-based threshold calibration from human approve/reject outcomes, with a **LightGBM + SHAP** calibrator running in **shadow mode** beside it — advisory, logged, never deciding (the documented, explainable path from rule to ML; a single tree overfits, so it's a regularised ensemble, and it declines when undertrained). **Deployed as two fully-isolated stacks** (separate Railway projects + Postgres) — a self-wiring public demo and a **forge-locked production** (refuses to seed, ship demo accounts, or run on non-persistent storage; the weak-admin refusal is regression-tested); **production-hardened** with row-locked write guards, a health-checked connection pool, and indexed hot paths so the guards hold under concurrency; each with its own [analytics cockpit](https://github.com/eugnmueller-87/SCM-POWER-BI). **Cost-intelligence layer:** a clean-sheet **should-cost engine** (components indexed to commodity markets → a defensible cost floor + target price, so you negotiate from *our* number, with DRAM/NAND sensitivity), and full per-asset **TCO** (acquisition + landed + deployment + lifetime OpEx + EOL − recovery) rolling up to a correctly-defined **TSCMC %** — deterministic engines, the LLM only proposes. **Spend analytics slice by year** — every euro traces from a received `Asset` back to its order line, so spend rolls up per calendar year (multi-year history, not one all-time blur). | [GitHub](https://github.com/eugnmueller-87/SCM-Master) · [Live Demo](https://scm-master-production.up.railway.app) |
| 📈 **SCM Power BI Cockpit** | AI-adoption **consulting case** for a non-technical CEO: *should a cloud/hosting enterprise invest in AI demand forecasting?* Synthetic-data generator → 7 internally-consistent CSVs feed a **live, auto-refreshing 7-tab web cockpit** (Node + Chart.js — Overview, SC Scorecard, Spend, Inventory, Forecast, **Should-Cost** margin-lever, **TCO**; cross-filter, click-to-drill KPIs, **per-year spend/forecast slicing** (a 5-year period selector where the data has a timeline — spend & backtest — with inventory honestly labelled a live snapshot, not a fake rewind), dynamic reorder alerts, forecast why-it-missed/how-to-fix diagnostics) **and** a Power BI report on the same live API — DAX measures anchored to **SCOR DS**, forecast accuracy (WMAPE / Bias / RMSE), should-cost & TCO. Backed by **cited market research** (Stanford AI Index, McKinsey, chip-geopolitics) and a **hype-vs-evidence** analysis driving an **invest / wait / pilot** recommendation, with a phased implementation plan + cost/timeline. | [GitHub](https://github.com/eugnmueller-87/SCM-POWER-BI) · [Live Dashboard](https://scm-power-bi-production.up.railway.app/) |
| 🔍 **Market intelligence sub-agent** | HERMES. Continuously crawls a curated watchlist of 56 AI suppliers across 8 categories via 5 crawlers (RSS, EDGAR, Tavily, Jobs, Earnings) — architecture scales to hundreds. Signals classified by Claude Haiku with delta tracking. Semantic RAG via Upstash Vector. Feeds supplier intelligence to Icarus and the knowledge brain on demand. | [GitHub](https://github.com/eugnmueller-87/hermes-agent) |
| ☠️Supplier due diligence agent | HADES. POST a company name, get a full risk report in under 2 minutes. 6 parallel LangGraph nodes: OFAC/UN sanctions, NorthData registry, LkSG/CSDDD signals, ESG, news sentiment, Hermes intel. Risk score 1–10 + Approve/Block recommendation. | [GitHub](https://github.com/eugnmueller-87/hades) |
| 📊 **Marketing Channel Statistical Analysis** | Full statistical pipeline for $500K marketing budget allocation across 7 channels. Welch t-tests, Bonferroni + BH-FDR correction, bootstrap CIs, Cohen's d. All 14 CPA pairs significant post-FDR. Executive memo with data-backed reallocation. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/Week%206/LAB%209/lab_statistical_analysis_eugen_mueller) |
| 🧪 **LLM Evaluation Framework** | LangSmith evaluation lab for procurement compliance Q&A. Custom 20-example dataset, LLM-as-judge correctness + completeness evaluators, A/B model comparison (gpt-4o-mini vs gpt-4o). | [GitHub](https://github.com/eugnmueller-87/Rating-System-for-AI-Responses) |

---

## Autonomous Agents & AI Systems

*Production multi-agent architectures and real-time AI applications running live.*

| Project/Description | GitHub |
|---|---|
| ⚡ **Pantheon OS — Autonomous Trading Orchestrator** — 8-agent system live on Hetzner, self-scheduling every 15 minutes. **ZEUS** orchestrates: **Icarus** (Hermes signal watcher) → **Hades** (OFAC/EU sanctions firewall) → **Artemis** (VIX + macro regime) → **Pythia** (Kelly-inspired position sizing) → **Zeus** (Claude Sonnet 4.6 reasoning + ChromaDB KB) → **Ares** (IBKR bracket orders: entry + 3% SL + 6% TP) → **Argus** (drawdown kill switch). **Apollo** runs daily: arXiv ingestion, earnings enrichment, self-improvement loop. Agent seniority system: TRAINEE → DIRECTOR, gated by verified win rate. Kafka event bus. Supabase + Grafana. | [GitHub](https://github.com/eugnmueller-87/Pantheon) |
| 🤖 **Icarus AI — Personal Operating System** — JARVIS-style AI OS via Telegram + an installable PWA. Async Claude tool-use agent loop over a modular skill layer: Gmail/Calendar (IMAP/CalDAV), voice input (Whisper), multimodal document analysis, live web search, LinkedIn drafting, expense tracking — plus on-demand procurement skills wiring in **Hades** (supplier due-diligence) and **Hermes** (market intelligence). Now also reaches my personal knowledge brain over **MCP** via a read-only `brain_search` skill — env-gated to run only on the local host next to the vault, so the cloud deployment has no vault access (local-first by construction). Multi-model routing (Sonnet/Haiku), per-session identity, prompt-injection hardening, persistent memory via Upstash Redis. | [GitHub](https://github.com/eugnmueller-87/Personal-Assistent) |
| 🧠 **Self-Improving Knowledge System** — A Claude-native knowledge OS built on a quality-gated ingest→distill→maintain loop. Stateful sync skills pull data into an immutable raw layer; a "distill-gate" blocks anything from entering the connected note graph until it's synthesized and linked (≥2 edges) — quality enforced at both ends. Capability layers: a portable harness that swaps the model behind Claude Code (cloud or **local LLM via LM Studio**, proven air-gapped) for private/offline work; a gated **overnight local-LLM batch worker** that drafts into quarantine and earns autonomy only after a 7-run quality streak (cloud model scores each run 1–10); **local hybrid retrieval** (vector + BM25 + RRF fusion + reranker) exposed to the agent over **MCP**, with a custom graph-fusion re-ranker that folds the wiki-link graph into search scoring; a two-tier passive-memory pipeline; a self-maintenance pass that audits the graph for orphans, broken links, and drift; and **agent-feed sync skills** that let the brain ingest its own procurement agents on demand — pulling Hermes' supplier intelligence and Hades' due-diligence verdicts into a fact-gated wiki library, with structural prompt-injection defense (no web-fetch tool in the ingest session). 100% local embeddings, zero per-query cost. Python · PowerShell · MCP · LM Studio · sqlite-vec/FTS5 · git-versioned. | [Private repo](https://github.com/eugnmueller-87/my-ai-brain) |

---

## Infrastructure & Security

*Self-hosted reliability and security tooling that keeps the production stack healthy — observe-only guardians, firewall hardening, and automated secret hygiene.*

| Project/Description | Repo |
|---|---|
| 🛡 **Lookout — Docker Host Guardian** — Observe-only watchdog for the production Docker hosts. Samples every container's CPU + memory each minute; on a sustained runaway it applies a reversible CPU cap (the only automatic action) and alerts via Telegram, leaving pause/restart/kill as owner-gated commands. Plus: firewall hardening (ufw + DOCKER-USER conntrack rules that actually block Docker-published ports), short-lived auto-rotated service tokens (no long-lived credentials on disk), a repo secret-scanner that watches all public repos for exposed keys, and a push-based health feed so the ops assistant can answer "are the servers running well?" in natural language. | [Private repo](https://github.com/eugnmueller-87/Lookout) |

## Client & Deployed Systems

*AI systems built and deployed for real organizations.*

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
| 📌 **Aushang** — Digitization for old-school German orgs (Kitas, Vereine, Kirchengemeinden, Kleingärten) that **changes none of their processes**: they keep pinning paper to a physical board; one admin photographs it from inside the tool, and members get a private feed, a shared calendar, an ICS subscription, and an email digest. **Privacy by construction** — the raw photo is OCR'd and PII-redacted **locally** (Tesseract + Microsoft Presidio + spaCy, fail-closed) before only the **redacted text** reaches the LLM (Claude, US — never raw images or PII; swappable to an EU model); raw photos and the LLM key never leave the FastAPI worker. **"The LLM advises, deterministic code decides"** — nothing reaches members without explicit admin confirmation, and all model output is schema-validated. Hardened to a four-layer security model (deny-by-default middleware → server role checks → SECURITY DEFINER RPCs → Postgres RLS + column-level REVOKE on PII), put through multi-agent **adversarial security reviews**. Next.js 16 + React 19 + Supabase (EU, RLS on every table), a Dockerized Python ML worker, a native **Android** app (Capacitor), and a one-command **self-host wizard**. | [GitHub](https://github.com/eugnmueller-87/DIGITNEWS)<br>[Self-host](https://github.com/eugnmueller-87/DIGITNEWS#self-host-run-your-own-copy) |
| ⚡ **Light-weight Transcriber** — Drop a YouTube URL or paste any text. Ask Claude anything about it. Answers without downloading the audio — paste a URL or text and ask. | [GitHub](https://github.com/eugnmueller-87/Light-weight-Transcriber) |

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
| 🧠 **TrueSpend Workflows (17)** — intake_receiver, chat_assistant, board_action, supplier_reply_handler, docusign_sign, docusign_callback, contract_watcher, reorder_trigger, hyperscaler_monitor, supplier_onboarding, invoice_processor, delivery_confirmation, asset_depreciation, llm_consumption, rag_embedder, dispatch_drain, vps_monitor. Production-grade: 120s timeouts, 3× retry, per-signal trace logging. Status transitions call SECURITY DEFINER RPCs — no workflow writes `tickets.status` directly. | [GitHub](https://github.com/eugnmueller-87/TrueSpend/tree/main/workflows) |
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
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat&logo=sqlalchemy&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat&logo=pydantic&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-FF6B35?style=flat)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=flat)
![Upstash Redis](https://img.shields.io/badge/Upstash%20Redis%20%26%20Vector-00C896?style=flat&logo=redis&logoColor=white)
![Claude API](https://img.shields.io/badge/Claude%20API-CC785C?style=flat)
![Claude Sonnet & Haiku](https://img.shields.io/badge/Claude%20Sonnet%20%26%20Haiku-CC785C?style=flat)
![MCP](https://img.shields.io/badge/MCP%20%28Model%20Context%20Protocol%29-CC785C?style=flat)
![OpenAI API](https://img.shields.io/badge/OpenAI%20API-412991?style=flat&logo=openai&logoColor=white)
![Mistral AI](https://img.shields.io/badge/Mistral%20AI-FA520F?style=flat&logo=mistralai&logoColor=white)
![Cohere](https://img.shields.io/badge/Cohere-39594D?style=flat)
![Whisper](https://img.shields.io/badge/Whisper-412991?style=flat&logo=openai&logoColor=white)
![Tavily](https://img.shields.io/badge/Tavily-1F6FEB?style=flat)
![LM Studio](https://img.shields.io/badge/LM%20Studio%20%28local%20LLM%29-4A25E1?style=flat)
![Ornith](https://img.shields.io/badge/Ornith%20%28local%20model%29-4A25E1?style=flat)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white)
![DocuSign](https://img.shields.io/badge/DocuSign%20eSignature-FFB600?style=flat&logo=docusign&logoColor=black)
![Telegram Bot API](https://img.shields.io/badge/Telegram%20Bot%20API-26A5E4?style=flat&logo=telegram&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat&logo=powershell&logoColor=white)
![Capacitor](https://img.shields.io/badge/Capacitor%20%28Android%29-119EFF?style=flat&logo=capacitor&logoColor=white)
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
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![LightGBM](https://img.shields.io/badge/LightGBM-9ACD32?style=flat)
![SHAP](https://img.shields.io/badge/SHAP%20%28explainability%29-8B5CF6?style=flat)
![statsforecast](https://img.shields.io/badge/Nixtla%20statsforecast-1A1A2E?style=flat)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)
![Data Visualization](https://img.shields.io/badge/Data%20Visualization-8B5CF6?style=flat)
![BI Dashboards](https://img.shields.io/badge/BI%20Dashboards-8B5CF6?style=flat)
![Demand Forecasting](https://img.shields.io/badge/Demand%20Forecasting-8B5CF6?style=flat)
![Should-Cost / TCO](https://img.shields.io/badge/Should--Cost%20%2F%20TCO-8B5CF6?style=flat)

**Security & Privacy**

![Local PII Redaction](https://img.shields.io/badge/Local%20PII%20Redaction-2E7D32?style=flat)
![Microsoft Presidio](https://img.shields.io/badge/Microsoft%20Presidio-0078D4?style=flat&logo=microsoft&logoColor=white)
![spaCy](https://img.shields.io/badge/spaCy-09A3D5?style=flat&logo=spacy&logoColor=white)
![Tesseract OCR](https://img.shields.io/badge/Tesseract%20OCR-5C6BC0?style=flat)
![Prompt-Injection Defense](https://img.shields.io/badge/Prompt--Injection%20Defense-B71C1C?style=flat)
![Row-Level Security](https://img.shields.io/badge/Postgres%20RLS-4169E1?style=flat&logo=postgresql&logoColor=white)

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

*10+ years in procurement, now building the AI systems I wished existed when I ran the function.*

# Hi, I'm Eugen 👋

### AI Solutions Consultant for Procurement: I turn procurement pain into working AI, and I demo it live. | Berlin 🇩🇪

> **The one-liner:** 15 years running procurement (portfolios to €60M, €10M+/yr savings) + an AI engineer who ships. I build the tools I wished existed when I ran the function, and every one below is live and clickable.

<!-- ▶ 2-min demo video: paste your Loom/YouTube link here. It's the single highest-impact addition to this profile -->

10+ years leading procurement and category management at **TeamViewer**, **Scout24**, **Foodpanda** and **Delivery Hero**, now engineering the AI systems that will transform the function I know inside out.

I don't just advise on AI transformation. I build the tools myself.

Every project here started from a real problem I encountered running procurement teams: manual triage, supplier compliance gaps, fragmented spend data, slow RFP cycles, and market intelligence that arrives too late. These are my answers, designed by someone who has lived them and built by someone who can now ship them.

AI Integration Bootcamp @ Ironhack · MBA-IT. I ship the tools, not just the slides. Every project below is live and demoable.

<p align="center">
  <img src="screenshot/procurement-ai-transformation-banner.png" alt="From manual, paper-bound procurement to an AI-automated, autonomous function, the transformation I build" width="100%">
</p>

---

## Procurement AI Transformation

*Every build below started from a real pain I lived running procurement teams. Read the table for the problem → what I built → the result; expand any project for the engineering depth.*

| # | Problem (the pain I lived) | What I built | Result | Links |
|---|---|---|---|---|
| 🧠 **TrueSpend** | Category managers drown in manual PR triage, scattered approvals across IT/legal/controlling, and spend nobody can see end-to-end. | An AI-native procurement OS running the full purchase-to-invoice lifecycle autonomously. | 17 autonomous workflows, intake→invoice hands-off, role-gated ops board, money-moves locked at the database layer. | [GitHub](https://github.com/eugnmueller-87/TrueSpend) · [Demo](https://intake-production-84a0.up.railway.app) |
| 📦 **SCM-Master** | Procurement, warehouse flow, and asset lifecycle live in disconnected systems: no single source of truth, no safe automation. | An AI-native supply-chain OS unifying all three, with an autonomous weekly purchasing run that a human still gates. | Auto-places demand-justified POs only at **≥0.90 confidence & <€200k**, proven by a 29-scenario agent-safety harness; CI-gated, twin-deployed. | [GitHub](https://github.com/eugnmueller-87/SCM-Master) · [Demo](https://scm-master-production.up.railway.app) |
| 📈 **SCM Power BI Cockpit** | A non-technical CEO asks "should we invest in AI demand forecasting?" and gets hype, not a decision. | A consulting-case cockpit: live 7-tab web dashboard + Power BI report on the same data, backed by cited research. | A defensible **invest / wait / pilot** recommendation with WMAPE/Bias accuracy, should-cost & TCO, and a phased plan. | [GitHub](https://github.com/eugnmueller-87/SCM-POWER-BI) · [Dashboard](https://scm-power-bi-production.up.railway.app/) |
| 🔴 **SpendLens** | Raw vendor spend arrives as messy CSVs: no classification, no compliance view, no supplier intelligence a category manager can act on. | A 5-stage AI pipeline: map → clean → classify vendors → flag compliance → surface supplier intel, across 7 decision screens. | Upload a spend file, get a classified, compliance-scored, DD-linked view, hardened for public deployment. | [GitHub](https://github.com/eugnmueller-87/PROCUREMENT) · [Demo](https://procurement-production-f940.up.railway.app) |
| 🤝 **Negotiation Agent** | Supplier negotiations anchor on price alone, so buyers leave win-win trades on the table, and nobody trusts an LLM to hold a walk-away line. | A **deployed** negotiation tool where the LLM has zero authority: a deterministic engine makes every accept/counter/walk-away call and fixes the exact figures a reply may state. A violating draft is rejected and redrafted server-side before it's ever sent. Real Opus writes the buyer's emails live; you play either seat. **Walk in prepared:** upload a contract → it extracts the deal (price, expiry, licenses, NDA/DPA), researches the supplier via my **Hades** agent, and proposes how the intelligence should *shape the mandate* (give/hold/hedge) via a deterministic rule table a human approves, so the LLM never edits the envelope. | At matched buyer cost, logrolling leaves the supplier **+0.27 utility** vs splitting the difference, a runnable eval. 183 tests, mypy-strict, CI-green, live on Railway. | [▶ Live demo](https://web-production-a5b7b.up.railway.app/) · [GitHub](https://github.com/eugnmueller-87/Negotiation-Agent) |
| ☠️ **Hades** | Supplier due-diligence (sanctions, registry, ESG, LkSG/CSDDD) takes analysts 1–2 days per supplier. | An autonomous agent that screens a company across 6 risk sources in parallel and returns a scored verdict. | **Full risk report in under 2 minutes:** sanctions/registry/ESG/news → risk score 1–10 + Approve/Block. | [GitHub](https://github.com/eugnmueller-87/hades) |
| 🔍 **Hermes** | Supplier market intelligence arrives too late: you learn a key supplier is in trouble after it hurts you. | A continuous market-intelligence agent watching a curated supplier list across 5 signal sources. | Tracks **56 AI suppliers across 8 categories**, classifies + delta-tracks signals, feeds DD and the CM on demand. | [GitHub](https://github.com/eugnmueller-87/hermes-agent) |
| 🏗 **Triage Agent** | Purchase requests pile up waiting for a human to route, compliance-check, and chase suppliers. | An autonomous agent that triages every PR: value-routes, checks NDA/DPA/MSA via RAG, runs RFQ/RFP outreach, recommends an award. | 6 importable n8n workflows replacing the manual triage queue end-to-end. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB4) |
| 📊 **Marketing Spend Stats** | A $500K budget is split across 7 channels on gut feel, not evidence. | A full statistical pipeline testing every channel-pair for real CPA difference. | All 14 CPA pairs significant post-FDR → an executive memo with a data-backed reallocation. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/Week%206/LAB%209/lab_statistical_analysis_eugen_mueller) |
| 🧪 **LLM Eval Lab** | "Is this AI answer actually good enough to trust for procurement compliance Q&A?", usually answered by vibes. | A LangSmith evaluation lab that scores answers objectively and A/B-compares models. | LLM-as-judge on correctness + completeness over a custom dataset; gpt-4o-mini vs gpt-4o compared on real numbers. | [GitHub](https://github.com/eugnmueller-87/Rating-System-for-AI-Responses) |

<details>
<summary><b>🔧 Engineering depth (click to expand, for technical reviewers)</b></summary>

- **TrueSpend:** n8n + Claude Sonnet 4.6 + PostgreSQL + React. 17 autonomous workflows, 32-table schema (dbmate-migrated), full P2I lifecycle. Role-gated Operations Board (procurement, IT, controlling, legal, admin). 4-agent compliance onboarding, DocuSign JWT Grant, Grafana, Jira ≥€100k. **DB-enforced security:** NOSUPERUSER PostgREST role, every status transition through SECURITY DEFINER RPCs, `PATCH tickets.status` → 403 at the database layer. **Agent security:** inbound email/invoices run under "the LLM advises, deterministic code decides", model output is schema-validated against an action allowlist, ticket/PO ids are derived deterministically (never from the model), and a prompt-injection repro proves the guard inert; money RPCs gated fail-closed off the browser token.
- **SpendLens:** React 18 SPA + FastAPI. 5-stage AI pipeline persisted to per-client SQLite (immutable raw layer, hash-dedup, recomputable enrichment). 7 screens wired to **Hades** and **Hermes**. **Security-hardened for public deployment:** opt-in shared-secret API auth (constant-time compare, docs disabled in prod), scoped CORS + full security-header/CSP middleware, chunked upload guards (type allowlist + 25 MB cap), per-IP rate limiting on Anthropic-billed endpoints, Pydantic-validated Hades proxy (SSRF surface closed), generic client errors with server-side logging. **Production-polished frontend:** React production builds + SRI, pre-paint theme, keyboard-accessible shell (focus-visible, ARIA), reduced-motion, error boundary that keeps the shell alive on crashes.
- **Negotiation Agent:** a **deployed** procurement negotiator ([▶ live](https://web-production-a5b7b.up.railway.app/)) where the LLM has zero authority. A stateless FastAPI backend runs the real deterministic engine: buyer utility `U = Σ wᵢ·vᵢ(xᵢ)`, acceptance on a **Boulware concession curve** (`(t/T)^β, β>1`, a spec bug I caught: the original exponent was inverted, conceding early and surrendering leverage), counteroffers via **logrolling** (an exact fractional-knapsack LP that concedes on terms the buyer weights lightly but the supplier values highly, not a price split). **The guard is mechanical, not a prompt:** each turn the server folds the transcript, the engine decides, Opus drafts the buyer's email, and a **guard-with-redraft loop** rejects any figure the engine didn't approve, a violating draft is redrafted (or replaced by a deterministic template) *before it's ever sent*. Real Opus (buyer) + Haiku (supplier); HMAC-signed mandates; you play either seat. **Contract intelligence, the "prepared buyer":** upload a contract → deep extraction (price, expiry, licenses, NDA/DPA, units) + supplier due-diligence via my deployed **Hades** agent → a **deterministic finding→mandate transform** (21 property tests) that proposes bounded, reversible envelope adjustments tagged give/hold/hedge, the LLM extracts and observes, a pure-Python rule table maps findings to deltas, and a **human approves the diff before signing**. That's *"LLM advises, code decides"* extended to mandate construction: the model's confidence is collapsed to a discrete assurance in Python first, so it never becomes a mandate number. Proven +0.27 supplier utility at matched buyer cost (runnable `neg-sim --baseline`); headless agent-vs-agent simulator with hidden-preference personas and bit-identical audit replay. **183 tests · 92.9% coverage · mypy --strict · CI green** (ubuntu+windows × py3.11–3.13). Architecture designed with Claude Fable 5; full design in [`docs/`](https://github.com/eugnmueller-87/Negotiation-Agent/tree/main/docs).
- **Hades:** POST a company name → 6 parallel LangGraph nodes: OFAC/UN sanctions, NorthData registry, LkSG/CSDDD signals, ESG, news sentiment, Hermes intel. Risk score 1–10 + Approve/Block recommendation, in under 2 minutes.
- **Hermes:** 5 crawlers (RSS, EDGAR, Tavily, Jobs, Earnings) over a curated 56-supplier / 8-category watchlist, architecture scales to hundreds. Signals classified by Claude Haiku with delta tracking. Semantic RAG via Upstash Vector.
- **SCM-Master:** FastAPI + SQLAlchemy 2.0 + Pydantic 2 (SQLite→Postgres), JWT role-gating, **52 test files · CI-gated ≥80% coverage**, 5-job CI (lint · Postgres · SAST · CVE-audit · agent-safety). Multi-sourcing core: `Product` decoupled from `ProductSupplier`, re-sourcing a line is one FK repoint. Serial-tracked `Asset` traced RECEIVED→…→DISPOSED with an unbroken link to its PO line. Autonomous weekly purchasing run under **"the LLM advises, deterministic code decides"**, the **confidence score is itself deterministic and audited**, gating auto-place at **≥0.90 & <€200k**, proven by a **29-scenario agent-safety harness** (unapproved supplier, over-cap spend, prompt injection, poisoned calibration → refuses every time). **Inventory science:** **Syntetos–Boylan** demand classifier → **Nixtla `statsforecast`** (Croston/SBA) with **conformal prediction-interval safety stock**, chosen over a hand-rolled TSB on a walk-forward benchmark; service-level safety stock (`z × σ`) + **ABC** class service levels. **Learning layer:** rule-based calibration from human approve/reject, with a **LightGBM + SHAP** calibrator in **shadow mode**, advisory, logged, never deciding. **Twin-deployed** (self-wiring public demo + forge-locked production that refuses to seed/ship demo accounts/run on non-persistent storage, regression-tested). **Cost-intelligence:** clean-sheet **should-cost engine** (commodity-indexed → defensible cost floor + target price, DRAM/NAND sensitivity) + per-asset **TCO** rolling up to **TSCMC %**, deterministic engines, the LLM only proposes.
- **SCM Power BI Cockpit:** synthetic-data generator → 7 internally-consistent CSVs feed a live auto-refreshing 7-tab web cockpit (Node + Chart.js) **and** a Power BI report on the same live API, DAX anchored to **SCOR DS**, forecast accuracy (WMAPE / Bias / RMSE), should-cost & TCO. Backed by cited research (Stanford AI Index, McKinsey, chip-geopolitics) driving a hype-vs-evidence invest/wait/pilot call with a phased plan + cost/timeline.
- **Triage Agent:** 5-tier value routing, supplier NDA/DPA/MSA compliance check via RAG, RFQ/RFP generation, multi-supplier outreach, evaluation matrix, award recommendation. 6 importable n8n workflows.
- **Marketing Spend Stats:** Welch t-tests, Bonferroni + BH-FDR correction, bootstrap CIs, Cohen's d across 7 channels / 14 CPA pairs.
- **LLM Eval Lab:** LangSmith, custom 20-example dataset, LLM-as-judge correctness + completeness evaluators, A/B (gpt-4o-mini vs gpt-4o).

</details>

<details>
<summary><b>📋 Case study: Hades, supplier due-diligence, framed as a client engagement</b></summary>

*How I'd scope, build, and hand off this solution for a procurement client, the way I'd run it as a consultant, not just a repo.*

**The problem.** Under Germany's LkSG (and the incoming EU CSDDD), every material supplier must be screened for sanctions, ownership, ESG, and human-rights risk, and re-screened on change. In most teams this is a 1–2 day manual analyst task per supplier: pull the registry, check OFAC/UN lists, scan news, cross-reference ESG databases, write it up. It doesn't scale, it's inconsistent between analysts, and it's the exact task that stalls onboarding.

**The approach.** I treated it as a decision-support problem, not a chatbot. The rule throughout: *the LLM advises, deterministic code decides.* Sanctions matching runs in deterministic code **before** the model sees anything, a hit forces `Block`, no LLM discretion. The model only summarizes and scores what verified sources return, so the output is defensible to an auditor.

**What I built.** An agent that takes a company name and runs 6 research pipelines in parallel, sanctions (OFAC SDN + UN), registry (NorthData), LkSG/CSDDD signals, ESG/labour, 90-day news sentiment, and live market intelligence, then returns a 1–10 risk score with an Approve / Conditional / Block recommendation and a plain-language executive summary, with a persistent audit trail.

**The result.** A 1–2 day analyst task becomes a **sub-2-minute, consistent, audit-trailed report**, the same rubric every time, defensible to compliance, and wired into the wider spend platform so a flagged supplier is caught at onboarding, not after.

**What I'd do for a client.** Scope their actual supplier master and risk appetite → map the screening rubric to *their* LkSG/CSDDD obligations → pilot on one high-risk category → tune the risk weights with their compliance team → integrate to their P2P so screening is a gate, not an afterthought. The tech is done; the engagement is the fit.

**See it:** [Hades repo](https://github.com/eugnmueller-87/hades)

</details>

---

## Autonomous Agents & AI Systems

*Production multi-agent architectures and real-time AI applications running live.*

| Project/Description | GitHub |
|---|---|
| ⚡ **Pantheon OS, Autonomous Trading Orchestrator:** 8-agent system live on Hetzner, self-scheduling every 15 minutes. **ZEUS** orchestrates: **Icarus** (Hermes signal watcher) → **Hades** (OFAC/EU sanctions firewall) → **Artemis** (VIX + macro regime) → **Pythia** (Kelly-inspired position sizing) → **Zeus** (Claude Sonnet 4.6 reasoning + ChromaDB KB) → **Ares** (IBKR bracket orders: entry + 3% SL + 6% TP) → **Argus** (drawdown kill switch). **Apollo** runs daily: arXiv ingestion, earnings enrichment, self-improvement loop. Agent seniority system: TRAINEE → DIRECTOR, gated by verified win rate. Kafka event bus. Supabase + Grafana. | [GitHub](https://github.com/eugnmueller-87/Pantheon) |
| 🤖 **Icarus AI: Personal Operating System.** A JARVIS-style AI OS on Telegram plus an installable PWA with streamed replies (SSE) and web push. An async Claude tool-use agent loop over a modular skill layer: **43 tools across 12 skill modules**, covering Gmail and Calendar (IMAP/CalDAV), voice input (Whisper), multimodal document analysis, live web search, LinkedIn drafting, GitHub issues and roadmap, maps and directions, shopping and expense logging, and YouTube transcript extraction. Procurement work is delegated to two sibling agents selectable in the same interface: **Hades** (supplier due-diligence, 4 tools) and **Hermes** (market intelligence, 12 tools). It also reaches my personal knowledge brain over **MCP**: search and read across the vault, plus one deliberately narrow write that appends to a staging inbox instead of the note graph, so captures cannot bypass the vault's own distill-gate. That whole vault layer is **never registered** unless `ICARUS_BRAIN_MCP=1`, which the cloud deployment never sets, so there is no code path from cloud to vault rather than a disabled one. Multi-model routing (Sonnet 5 / Haiku), per-session identity scoped to an owner id, prompt-injection hardening, persistent history and sessions on Upstash Redis. **Also self-hosted:** a second instance runs 24/7 on hardware I own with local embeddings and a private mesh network, see the case study below. | [GitHub](https://github.com/eugnmueller-87/Personal-Assistent) |
| 🧠 **Self-Improving Knowledge System:** A Claude-native knowledge OS built on a quality-gated ingest→distill→maintain loop. Stateful sync skills pull data into an immutable raw layer; a "distill-gate" blocks anything from entering the connected note graph until it's synthesized and linked (≥2 edges), quality enforced at both ends. Capability layers: a portable harness that swaps the model behind Claude Code (cloud or **local LLM via LM Studio**, proven air-gapped) for private/offline work; a gated **overnight local-LLM batch worker** that drafts into quarantine and earns autonomy only after a 7-run quality streak (cloud model scores each run 1–10); **local hybrid retrieval** (vector + BM25 + RRF fusion + reranker) exposed to the agent over **MCP**, with a custom graph-fusion re-ranker that folds the wiki-link graph into search scoring; a two-tier passive-memory pipeline; a self-maintenance pass that audits the graph for orphans, broken links, and drift; and **agent-feed sync skills** that let the brain ingest its own procurement agents on demand, pulling Hermes' supplier intelligence and Hades' due-diligence verdicts into a fact-gated wiki library, with structural prompt-injection defense (no web-fetch tool in the ingest session). 100% local embeddings, zero per-query cost. Python · PowerShell · MCP · LM Studio · sqlite-vec/FTS5 · git-versioned. | [Private repo](https://github.com/eugnmueller-87/my-ai-brain) |

<details>
<summary><b>🏠 Case study: ICARUS self-hosted, a private, always-on AI assistant on hardware I own</b></summary>

*The full build: local inference host, private mesh networking, and the service layer that keeps it up unattended. Written the way I'd hand it to a client who says "we can't put that data in someone else's cloud."*

**The problem.** A personal AI assistant is only useful if it knows your actual context, notes, decisions, calendar, client thinking. That is exactly the data you cannot paste into a hosted chatbot. So you pick one: an assistant that's useful and your data leaves the building, or one that's private and blind. For regulated procurement work that's not a real choice.

**The approach.** Split on the trust boundary, not on convenience. **Two instances, one codebase.** The cloud instance is blind *by construction*: the vault tool isn't gated at runtime, it's **never registered** unless `ICARUS_BRAIN_MCP=1`, which the cloud deployment never sets, so there is no code path from the cloud to the vault, not merely a disabled one. The second instance runs on hardware I own, sits next to the vault, and reaches my phone over a private mesh network. Nothing is published to the internet.

**The hardware, deliberately unglamorous.** A **2018 Intel MacBook Pro** (i7-8559U, 8 threads, 16GB RAM, **no GPU**), clamshell, on AC, never sleeping (`pmset -c standby 0 disablesleep 1`). The lesson I'd give a client: private AI infrastructure doesn't need a GPU rig, it needs an honest split of *what runs where*. I benchmarked a 7B model on this box at **~5 tok/s** and drew the line there: **embeddings and retrieval run locally; heavy generation does not.** Right-sizing beats wishful hardware.

**The stack that actually runs.**
- **Ollama** on `127.0.0.1:11434` serving **`nomic-embed-text`**, 100% local embeddings, zero per-query cost, loopback-bound so it's unreachable off-box. *(I tried LM Studio first; it failed on this Intel generation. Ollama was the robust call, documented, not glossed over.)*
- **Hybrid retrieval** over the vault, vector + BM25 + **RRF fusion**, **783 notes** indexed locally.
- **FastAPI + uvicorn** serving an installable **PWA** (web manifest + service worker) on `:8080`.
- **Python 3.12** in a venv, the system 3.9 was too old.
- **Tailscale** (WireGuard mesh), my phone reaches the Mac at a stable private address from anywhere. No port forwarding, no inbound firewall rule, nothing public.

**The networking decision worth reading.** The obvious path was a Cloudflare Tunnel on my own domain. I costed it and **rejected it**: an external CNAME to `cfargotunnel.com` requires Cloudflare's **Business plan (~$200/mo)**, and the only free route is migrating the domain's nameservers, which would drag a live production site and business email (MX/SPF/DKIM) along for the sake of a personal tool. Tailscale delivered the same outcome with **zero DNS changes, nothing publicly exposed, and only my own devices on the network.** Choosing the boring option that doesn't put production at risk *is* the engineering.

**Reliability, three `launchd` services, each solving a different failure.**
- **`de.icarus.pwa`:** `RunAtLoad` + `KeepAlive`. A wrapper forces `PATH`, loads the environment, and **waits up to 60s for Ollama** before `exec`-ing uvicorn so launchd owns the PID and boot ordering can't race. *Verified by killing the process: back up in ~14 seconds.*
- **`de.brain.sync`:** nightly at 04:00: `git pull --ff-only` → reindex. **Fails safe**, if the pull fails it *skips* the reindex rather than indexing a half-updated state. A stale index beats a corrupt one.
- **`de.icarus.health`:** every 15 min, polls `/health` and pushes to my phone **only on state change**. Two deliberate design calls: (1) a watchdog that reports "all good" every 15 minutes gets muted within a week, and **a muted alert channel is strictly worse than none, it creates the belief you'd be told**; (2) the fingerprint is *status + failing-dependency list*, so a **new** dependency breaking while already degraded still fires. It also catches the failure `KeepAlive` structurally cannot: a **wedged** process never crashes, so it's never restarted, it just holds the port and answers nothing.

**Verified, not assumed.** A full unattended reboot test: Ollama, the launchd agents, uvicorn, and the mesh all came back with nobody touching the machine, and the PWA answered from another device. The bug that cost the most: login returned `200` and every subsequent request `401`, the session cookie was hardcoded `secure=True`, which browsers silently drop over plain HTTP. Now environment-controlled, so local HTTP testing and Secure-cookie production are the same code.

**The result.** An assistant that reads my live private knowledge base, runs 24/7 on a seven-year-old laptop, costs **€0/month** in inference and hosting, is reachable from my phone anywhere in the world, self-restarts, self-refreshes its index nightly, and tells me when it's genuinely unwell. No vendor holds the data.

**What I'd do for a client.** Map their actual trust boundary first, which data legally *cannot* leave, which comfortably can. Put the local-only tools behind registration-time gating so "private" is structural, not a config checkbox someone can flip. Size the local hardware to embeddings + retrieval, keep heavy generation wherever their policy allows. Then the unglamorous 80%: supervision, fail-safe ordering, and alerting people won't mute. The demo is a day; the part that survives contact with production is the service layer.

**See it:** [ICARUS repo](https://github.com/eugnmueller-87/Personal-Assistent)

</details>

---

## Infrastructure & Security

*Self-hosted reliability and security tooling that keeps the production stack healthy, observe-only guardians, firewall hardening, and automated secret hygiene.*

| Project/Description | Repo |
|---|---|
| 🛡 **Lookout, Docker Host Guardian:** Observe-only watchdog for the production Docker hosts. Samples every container's CPU + memory each minute; on a sustained runaway it applies a reversible CPU cap (the only automatic action) and alerts via Telegram, leaving pause/restart/kill as owner-gated commands. Plus: firewall hardening (ufw + DOCKER-USER conntrack rules that actually block Docker-published ports), short-lived auto-rotated service tokens (no long-lived credentials on disk), a repo secret-scanner that watches all public repos for exposed keys, and a push-based health feed so the ops assistant can answer "are the servers running well?" in natural language. | [Private repo](https://github.com/eugnmueller-87/Lookout) |

## Client & Deployed Systems

*AI systems built and deployed for real organizations.*

| Project/Description | GitHub |
|---|---|
| 📊 **Client Dashboard:** Internal agency dashboard for monitoring all live client AI systems. Real-time status, deployment health, pipeline metrics across projects. | [GitHub](https://github.com/eugnmueller-87/CLIENT-DASHBOARD) |
| 🧙 **Agency Wizard:** Internal onboarding wizard for deploying full AI automation stacks to clients in a single 3-hour session. Validates every credential live, then provisions into the client's own n8n Cloud instance. | [GitHub](https://github.com/eugnmueller-87/Agency-Wizard) |
| 🩺 **AI Triage System (Metabelly):** Autonomous customer support triage for a Croatian gut health brand. Incoming emails classified by AI (category, priority, language), auto-replies drafted, Calendly links appended, results routed to Slack. n8n + Mistral AI + Gmail API. GDPR-compliant. | [GitHub](https://github.com/eugnmueller-87/Metabelly) |
| 📧 **Noosphr Email Router:** AI email triage for Noosphr's inbox. Claude Haiku classifies and routes to `#business`, `#support`, or `#spam` Slack channels with one-click reply buttons. Runs as systemd service on Hetzner VPS. | [GitHub](https://github.com/eugnmueller-87/Noosphr-Workspace) |

---

## Full-Stack AI Applications

| Project/Description | GitHub |
|---|---|
| 🏥 **Kita Connect:** Full-stack daycare management platform for German Kitas. ~€0/month, GDPR-compliant, Frankfurt-hosted. Three portals: parents, educators (AI-assisted learning stories via Claude Haiku), management (multi-channel comms, automated registrations). | [GitHub](https://github.com/eugnmueller-87/kita-connect) |
| 📌 **Aushang:** Digitization for old-school German orgs (Kitas, Vereine, Kirchengemeinden, Kleingärten) that **changes none of their processes**: they keep pinning paper to a physical board; one admin photographs it from inside the tool, and members get a private feed, a shared calendar, an ICS subscription, and an email digest. **Privacy by construction**, the raw photo is OCR'd and PII-redacted **locally** (Tesseract + Microsoft Presidio + spaCy, fail-closed) before only the **redacted text** reaches the LLM (Claude, US: never raw images or PII; swappable to an EU model); raw photos and the LLM key never leave the FastAPI worker. **"The LLM advises, deterministic code decides"**: nothing reaches members without explicit admin confirmation, and all model output is schema-validated. Hardened to a four-layer security model (deny-by-default middleware → server role checks → SECURITY DEFINER RPCs → Postgres RLS + column-level REVOKE on PII), put through multi-agent **adversarial security reviews**. Next.js 16 + React 19 + Supabase (EU, RLS on every table), a Dockerized Python ML worker, a native **Android** app (Capacitor), and a one-command **self-host wizard**. | [GitHub](https://github.com/eugnmueller-87/DIGITNEWS)<br>[Self-host](https://github.com/eugnmueller-87/DIGITNEWS#self-host-run-your-own-copy) |
| ⚡ **Light-weight Transcriber:** Drop a YouTube URL or paste any text. Ask Claude anything about it. Answers without downloading the audio, paste a URL or text and ask. | [GitHub](https://github.com/eugnmueller-87/Light-weight-Transcriber) |

---

## RAG, LangChain & LangGraph

| Project/Description | GitHub |
|---|---|
| 📚 **RAG Pipeline:** Chunking, embedding, retrieval with metadata filtering. Upstash Vector, OpenAI embeddings, query pipeline with source tracking. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%202) |
| ⚖️ **Relevance Scoring & Rerankers:** Advanced RAG over EU AI Act legal text. Vector similarity, metadata filtering, Cohere cross-encoder reranking, before/after position-shift analysis. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%203/LAB%203) |
| 🤖 **LangChain Tool-Use Agent:** ReAct-pattern agent with free tool selection across 4 custom tools. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%202) |
| 🔄 **LangGraph Complaint Processor:** Deterministic 5-node state machine with human-in-the-loop checkpoints. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%203/LAB%204) |

---

## Workflow Automation (n8n)

| Project/Description | GitHub |
|---|---|
| 🧠 **TrueSpend Workflows (17):** intake_receiver, chat_assistant, board_action, supplier_reply_handler, docusign_sign, docusign_callback, contract_watcher, reorder_trigger, hyperscaler_monitor, supplier_onboarding, invoice_processor, delivery_confirmation, asset_depreciation, llm_consumption, rag_embedder, dispatch_drain, vps_monitor. Production-grade: 120s timeouts, 3× retry, per-signal trace logging. Status transitions call SECURITY DEFINER RPCs: no workflow writes `tickets.status` directly. | [GitHub](https://github.com/eugnmueller-87/TrueSpend/tree/main/workflows) |
| 🏗 **Procurement Triage Workflows:** 6 importable n8n workflows: PR ingestion, tier routing, ERP budget/PO, RFQ/RFP outreach, quote collection, approval handling. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/LAB4/n8n_workflows) |
| 📰 **arXiv Research Summarizer:** n8n + Claude + Notion. POST an arXiv URL → fetch metadata → Claude summary → Notion record. | [GitHub](https://github.com/eugnmueller-87/IRONHACK/tree/main/WEEK%204/EXTRA%202) |

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
![uvicorn](https://img.shields.io/badge/uvicorn-499848?style=flat)
![Ollama](https://img.shields.io/badge/Ollama%20%28local%20LLM%29-000000?style=flat&logo=ollama&logoColor=white)
![Local Embeddings](https://img.shields.io/badge/Local%20Embeddings%20%28nomic--embed--text%29-4A25E1?style=flat)
![Hybrid Retrieval](https://img.shields.io/badge/Hybrid%20Retrieval%20%28BM25%20%2B%20Vector%20%2B%20RRF%29-FF6B35?style=flat)
![sqlite-vec](https://img.shields.io/badge/sqlite--vec%20%2F%20FTS5-003B57?style=flat&logo=sqlite&logoColor=white)
![Claude Opus](https://img.shields.io/badge/Claude%20Opus-CC785C?style=flat)
![Claude Code](https://img.shields.io/badge/Claude%20Code-CC785C?style=flat)
![PWA](https://img.shields.io/badge/PWA%20%26%20Service%20Workers-5A0FC8?style=flat&logo=pwa&logoColor=white)
![IMAP / CalDAV](https://img.shields.io/badge/IMAP%20%2F%20CalDAV-1F6FEB?style=flat)
![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=flat&logo=obsidian&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat&logo=gnubash&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

**Infrastructure & Self-Hosting**

![Self-Hosted AI](https://img.shields.io/badge/Self--Hosted%20AI%20Infrastructure-0F766E?style=flat)
![Tailscale](https://img.shields.io/badge/Tailscale-242424?style=flat&logo=tailscale&logoColor=white)
![WireGuard](https://img.shields.io/badge/WireGuard%20Mesh%20VPN-88171A?style=flat&logo=wireguard&logoColor=white)
![launchd](https://img.shields.io/badge/macOS%20%2F%20launchd-000000?style=flat&logo=apple&logoColor=white)
![systemd](https://img.shields.io/badge/Linux%20%2F%20systemd-FCC624?style=flat&logo=linux&logoColor=black)
![SSH](https://img.shields.io/badge/SSH%20%2F%20Remote%20Ops-0F766E?style=flat)
![Scheduled Jobs](https://img.shields.io/badge/Cron%20%2F%20Scheduled%20Jobs-0F766E?style=flat)
![Health Monitoring](https://img.shields.io/badge/Health%20Checks%20%26%20Watchdogs-F46800?style=flat)
![ntfy](https://img.shields.io/badge/ntfy%20%28push%20alerting%29-317F6F?style=flat)
![VPS Deployment](https://img.shields.io/badge/VPS%20Deployment-D50C2D?style=flat)

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
![Local-First Architecture](https://img.shields.io/badge/Local--First%20Architecture-2E7D32?style=flat)
![Zero-Trust Networking](https://img.shields.io/badge/Zero--Trust%20Networking-B71C1C?style=flat)
![Data Residency](https://img.shields.io/badge/Data%20Residency%20%26%20Trust%20Boundaries-2E7D32?style=flat)
![EU AI Act](https://img.shields.io/badge/EU%20AI%20Act%20%28deployer%20compliance%29-003399?style=flat)

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

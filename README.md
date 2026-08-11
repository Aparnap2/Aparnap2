# Hi, I'm Aparna Pradhan.

### Applied AI Architect & Full-Stack Engineer




< a href="https://www.credly.com/badges/a7f40199-2c96-473e-9057-af20af5924e4/public_url" target="_blank">
<img width="900" height="550" alt="2025-04-27" src="https://github.com/Aparnap2/Aparnap2/blob/main/cN%2Bb_LtQNnJrj9jnfxxqyGZKUNSlgZOqOSyi2TqtCKk%3D.png" />
</a>

<div align="left">
  <a href="https://aparnapradhanportfolio.netlify.app/" target="_blank">
    <img src="https://img.shields.io/badge/Portfolio-View_Case_Studies-000000?style=for-the-badge&logo=vercel" alt="Portfolio" />
  </a>
  <a href="https://www.linkedin.com/in/aparna-pradhan-06b882215/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin" alt="LinkedIn" />
  </a>
  <a href="mailto:softservicesinc.portfolio@gmail.com">
    <img src="https://img.shields.io/badge/Email-Hire_Me-EA4335?style=for-the-badge&logo=gmail" alt="Email" />
  </a>
</div>

---

### 🏛️ The Engineering Philosophy
> **"Outcomes over demos. Architecture over hype."**

I bridge the gap between fragile AI research demos and resilient enterprise systems. I don't just write prompts; I engineer **stateful, observable, and governed architectures** that replace manual operational toil with deterministic reliability.

**My systems are built for:**
*   **Predictability:** End-to-end type safety (Pydantic/TypeScript) and binary acceptance tests.
*   **Governance:** Strict "Human-in-the-Loop" (HITL) gates, RBAC, and audit trails.
*   **Observability:** If it isn't traced in Langfuse or Temporal UI, it doesn't exist.

---

### 🛠️ The Architecture Stack

| Layer | Technology Choice | Why? |
| :--- | :--- | :--- |
| **Orchestration** | ![LangGraph](https://img.shields.io/badge/LangGraph-State_Machines-ff69b4?style=flat-square) ![Temporal](https://img.shields.io/badge/Temporal-Durable_Workflows-blue?style=flat-square) | Deterministic loops & durable execution, not random chains. |
| **Backend Core** | ![FastAPI](https://img.shields.io/badge/FastAPI-Async_Python-009688?style=flat-square) ![Go](https://img.shields.io/badge/Go-Fiber-00ADD8?style=flat-square) ![Hono](https://img.shields.io/badge/Hono-Bun-E36002?style=flat-square) | High-concurrency async I/O for parallel agent execution. |
| **Data Fabric** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-PgVector-336791?style=flat-square) ![Qdrant](https://img.shields.io/badge/Qdrant-VectorDB-DC244C?style=flat-square) | Hybrid Search (Vector + FTS) for grounded truth retrieval. |
| **Observability** | ![Langfuse](https://img.shields.io/badge/Langfuse-Tracing-blue?style=flat-square) ![Grafana](https://img.shields.io/badge/Grafana-Metrics-F46800?style=flat-square) | Full visibility into latency, cost per token, and trace failures. |
| **Cloud** | ![Azure](https://img.shields.io/badge/Azure-AI_Foundry-0078D4?style=flat-square) ![Docker](https://img.shields.io/badge/Docker-Containers-2496ED?style=flat-square) | Azure-native deployments, container-first infrastructure. |

---

### 🚀 Production-Grade Architectures

#### 1. [Invoicify: Azure-Native AP Automation with MCP](https://github.com/Aparnap2/invoicify)
*Autonomous Accounts Payable agent replacing manual invoice processing end-to-end.*

[![Tests](https://img.shields.io/badge/tests-83%20passing-brightgreen)](https://github.com/Aparnap2/invoicify) [![MCP](https://img.shields.io/badge/MCP-QuickBooks%20%7C%20HubSpot-purple)](https://modelcontextprotocol.io)

> **The Problem:** Finance teams drown in manual invoice reconciliation — 15–30 min per invoice, 5–10% error rate, 3–7 day approval bottleneck.
> **The Solution:** A **"Trust Battery"** architecture with Azure OCR + LangGraph state machine that autonomously approves low-risk invoices and escalates anomalies.

*   **Architecture:** `PDF Upload` → `Azure Document Intelligence (OCR)` → `LangGraph AP Workflow (11 nodes)` → `Trust Battery Decision` → `QuickBooks MCP + HubSpot MCP Sync` → `Immutable Audit Ledger`
*   **Key Innovation:** **Trust Battery Logic** — 4-level vendor trust (PROBATION → STANDARD → CORE → STRATEGIC) with dynamic auto-approval thresholds ($500 → $50k). Bank detail changes and PO mismatches auto-route to HITL review tasks.
*   **Production Hardening:** Idempotent MCP tool calls via `Request-Id` headers, SHA-256 cryptographic audit receipts, SOC 2 data minimization (store hashes, not PDFs), Azure Key Vault secret management, L1/L2/L3 LLM cache (90% call reduction).
*   **Metrics:** **99% OCR accuracy** | **60–80% auto-approval rate** | **97% cost reduction** ($15–30 → $0.50/invoice) | **83 tests passing** | **$0/month for 12 months** (Azure free tier)

---

#### 2. [Sarthi.ai: Internal Ops Virtual Office](https://github.com/Aparnap2/sarthi_ai)
*Governance-first internal operations system for Seed to Series A startups replacing back-office fragmentation with 13 specialized AI employees.*

[![Tests](https://img.shields.io/badge/tests-125%20passing-brightgreen)](https://github.com/Aparnap2/sarthi_ai) [![Desks](https://img.shields.io/badge/desks-6%20Active-blue)](https://github.com/Aparnap2/sarthi_ai)

> **The Problem:** Early-stage startups drown in operational chaos, juggling 15 disconnected tools. Founders waste 15–20 hours/week on back-office tasks, delaying product roadmaps by ~3 months per year.
> **The Solution:** A virtual office with a **Chief of Staff** orchestrating 13 specialized AI employees across 6 desks (Finance, People, Legal, Intelligence, IT, Admin). Everything requiring human judgment is prepared perfectly and presented in 30 seconds.

*   **Architecture:** `Telegram Bot` → `Tier 1: Chief of Staff Agent` → `Tier 2: 6 Desks (13 Virtual Employees)` → `Tier 0: BusinessOS (Go + Temporal + Graphiti)` → `Tier 3: Data Layer (Qdrant + Neo4j)`.
*   **Key Innovation:** **The Self-Correcting Memory System** — Sarthi learns company-specific context over time. Agent acts → Founder confirms → Memory updated (Qdrant + Neo4j) → Future auto-categorized with context drift detection.
*   **Production Hardening:** Strict HITL (Human-in-the-Loop) gates enforced by Temporal, deterministic state management, and an explicit boundary (Zero external-facing work like RevOps or Customer Success).
*   **Metrics:** **$0/month infrastructure cost** for MVP | **Replaces ₹2L–₹3.75L/month** in fractional admin costs | **20x–50x ROI** | **125 tests passing** (Targeting 189 tests for v4.2.0).

---

#### 3. [TechTrend: Agentic Commerce Platform](https://github.com/Aparnap2/smart_commerce_agent)
*Production-grade AI-native e-commerce CX platform where the agent IS the interface — zero page navigation, zero forms, all conversation.*

[![Tests](https://img.shields.io/badge/tests-307%20passing-brightgreen)](https://github.com/Aparnap2/smart_commerce_agent) [![Pass Rate](https://img.shields.io/badge/pass%20rate-100%25-brightgreen)](https://github.com/Aparnap2/smart_commerce_agent)

> **The Problem:** Chatbots are dumb text boxes that can't "do" anything — users still navigate pages, fill forms, and wait for human support agents.
> **The Solution:** A **Generative UI** agent that renders dynamic React components (ProductGrid, CartCanvas, OrderTimeline, ActionConfirm) directly inside the chat stream, powered by a LangGraph supervisor routing 14 intent types.

*   **Architecture:** `Next.js 15 GenUI Canvas` → `Hono + Bun (GraphQL Yoga / MCP endpoints)` → `FastAPI + LangGraph (ShopperAgent / SupportAgent)` → `PostgreSQL 16 + pgvector (Hybrid FTS + Vector Search)` → `Azure AI Foundry (gpt-4o-mini)`
*   **Key Innovation:** **Agent-First Commerce** — Every user action is a conversation turn. LangGraph supervisor with typed state, Redis checkpointing, circuit breaker for resilience, and Human-in-the-Loop for critical actions (checkout, refunds). RAGAS + LLM-as-Judge scoring via Langfuse.
*   **Observability:** 100% of agent turns traced in Langfuse with per-span latency (classify, tools, generate), faithfulness scores, and correlation IDs on every tool call.
*   **Metrics:** **307 tests passing (100% pass rate)** | **P95 agent turn latency < 500ms** | **Task completion target > 95%** | **Cart recovery > 15%** vs 10% industry avg | **Merchant time saved > 2hr/day**

---

<div align="center">
  <sub><em>"We cannot solve our problems with the same thinking we used when we created them."</em> – Albert Einstein</sub>
</div>

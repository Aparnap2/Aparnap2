# Hi, I'm Aparna Pradhan.

### Applied AI Architect & Full-Stack Engineer
#### *Building Governance-First Autonomous Systems.*



<img width="900" height="550" alt="2025-04-27" src="https://github.com/user-attachments/assets/3bdf9974-1793-46c8-9e91-a1868658c1e9" />



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

#### 2. [IterateSwarm OS: Autonomous Engineering Organization](https://github.com/Aparnap2/IterateSwarm)
*Polyglot, event-driven agent swarm that transforms unstructured feedback into production-ready code changes — fully automated, no third-party dependencies required.*

[![Tests](https://img.shields.io/badge/tests-156%20passing-brightgreen)](https://github.com/Aparnap2/IterateSwarm) [![Services](https://img.shields.io/badge/services-11%20running-blue)](https://github.com/Aparnap2/IterateSwarm)

> **The Problem:** Engineering teams lose hours triaging noisy feedback, manually writing GitHub issues, and waiting on slow human-gated review cycles.
> **The Solution:** A **"Council of Agents"** (Supervisor, Researcher, SRE, SWE, Reviewer, Triage) orchestrated by Temporal that deduplicates feedback semantically, drafts structured specs, and proposes production-ready PRs — humans only click Approve.

*   **Architecture:**
    ```mermaid
    graph LR
    A[Discord / SwarmChat] --> B(Go Gateway: Fiber)
    B --> C[(Redpanda / Kafka)]
    C --> D(Temporal Workflow)
    D -->|gRPC| E(Python LangGraph Agents)
    E --> F[(Qdrant: Semantic Dedup)]
    D --> G{HITL Approval}
    G --> H[SwarmRepo / GitHub PR]
    ```
*   **Key Innovation:** **Native Platform (SwarmChat + SwarmRepo)** — Adapter-pattern replacements for Discord and GitHub that speak their API dialects. Swap real Discord/GitHub via a single env var. Zero vendor lock-in at the infrastructure level.
*   **Polyglot Stack:** Go (Fiber, Temporal Worker, gRPC client) + Python (LangGraph, gRPC server, 6 agents) + Redpanda + Qdrant + PostgreSQL + Grafana. Type-safe cross-language contracts via Protocol Buffers.
*   **Metrics:** **156 tests passing** | **End-to-end latency < 3s** | **11 production services** | **48-hour HITL timeout** with Dead Letter Queue after 5 failed attempts

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

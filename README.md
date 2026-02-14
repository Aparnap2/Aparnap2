# Hi, I'm Aparna Pradhan.

### Applied AI Architect & Full-Stack Engineer
#### *Building Governance-First Autonomous Systems.*



<img width="2000" height="1414" alt="2025-04-27" src="https://github.com/user-attachments/assets/3bdf9974-1793-46c8-9e91-a1868658c1e9" />



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
*   **Observability:** If it isn't traced in Langfuse, it doesn't exist.

---

### 🛠️ The Architecture Stack

| Layer | Technology Choice | Why? |
| :--- | :--- | :--- |
| **Orchestration** | ![LangGraph](https://img.shields.io/badge/LangGraph-State_Machines-ff69b4?style=flat-square) ![LiteLLM](https://img.shields.io/badge/LiteLLM-Gateway-orange?style=flat-square) | Deterministic loops, not random chains. Cost-controlled routing. |
| **Backend Core** | ![FastAPI](https://img.shields.io/badge/FastAPI-Async_Python-009688?style=flat-square) ![NestJS](https://img.shields.io/badge/NestJS-Enterprise_Node-E0234E?style=flat-square) | High-concurrency async I/O for parallel agent execution. |
| **Data Fabric** | ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-PgVector-336791?style=flat-square) ![Neo4j](https://img.shields.io/badge/Neo4j-GraphRAG-008CC1?style=flat-square) | Hybrid Search (Vector + Graph) for grounded truth retrieval. |
| **Observability** | ![Langfuse](https://img.shields.io/badge/Langfuse-Tracing-blue?style=flat-square) ![Docker](https://img.shields.io/badge/Docker-Containers-2496ED?style=flat-square) | Full visibility into latency, cost per token, and trace failures. |

---

### 🚀 Production-Grade Architectures

#### 1. [Invoicify: Autonomous Finance Operations](https://github.com/Aparnap2/invoicify)
*Vertical AI Agent for AP/AR Automation replacing manual data entry.*

> **The Problem:** Finance teams drown in manual invoice reconciliation and "email ping-pong."
> **The Solution:** A **"Trust Battery"** architecture that autonomously approves low-risk invoices and escalates anomalies.

*   **Architecture:** `Analyst-Critic Loop` (LangGraph) → `Slack Intern UI` → `ERP Sync`
*   **Key Innovation:** **Trust Battery Logic**—Dynamic confidence thresholds that increase autonomy over time per vendor.
*   **Metric:** Reduced manual review by **80%** with **100%** auditability on escalations.

#### 2. [ExecOps: Event-Driven Infrastructure Guard](https://github.com/Aparnap2/ExecOps)
*Event-driven multi-agent system for DevOps & Compliance governance.*

> **The Problem:** Alerts are noisy, and manual remediation is slow and risky.
> **The Solution:** A specialized **"Council of Agents"** that triages webhooks and proposes idempotent fixes.

*   **Architecture:**
    ```mermaid
    graph LR
    A[Webhook Event] --> B(Sentinel: PR Audit)
    A --> C(Hunter: EBS Cleanup)
    B & C --> D{Action Proposal}
    D --> E[Human Inbox Approval]
    ```
*   **Key Innovation:** **Idempotent Action Proposals**—Agents cannot "act," only "propose." Humans click "Approve" to execute via secure runners.
*   **Agents:** `Sentinel` (Code Quality), `Hunter` (Cost Ops), `Guard` (IAM Security).

#### 3. [Smart Commerce: GenUI Support Protocol](https://github.com/Aparnap2/smart_commerce_agent)
*Next-gen e-commerce support with Generative UI and Universal Commerce Protocol (UCP).*

> **The Problem:** Chatbots are dumb text boxes that can't "do" anything.
> **The Solution:** A **Generative UI** agent that renders dynamic React components (Refund Cards, Product Carousels) inside the chat.

*   **Architecture:** `RAG (Vercel AI SDK)` → `MCP Tool Execution` → `GenUI Render`
*   **Key Innovation:** **Universal Commerce Protocol (UCP)**—Standardized schema for product discovery and support actions across platforms.
*   **Tech:** RAG with Prisma, Vercel AI SDK, React Server Components.

---

### 🤝 Engagement Strategy
I partner with technical founders to build **assets**, not technical debt.

1.  **Audit (Week 1):** I review your legacy automations/codebase. Output: Latency/Cost Baseline & Architecture Plan.
2.  **Build (Weeks 2-4):** Sprints focused on passing binary acceptance tests. No "it works on my machine."
3.  **Handover:** Full documentation, architectural decision records (ADRs), and ops dashboards.

---

<div align="center">
  <sub><em>"We cannot solve our problems with the same thinking we used when we created them."</em> – Albert Einstein</sub>
</div>

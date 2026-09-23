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

# Hi, I'm Aparna Pradhan

### Applied AI Engineer · Agentic Systems · Enterprise AI Integration

I build **AI systems for real business workflows** — combining agentic reasoning with deterministic software, enterprise integrations, evaluation, reliability, and human oversight.

My interest is at the intersection of:

**Applied AI × Systems Engineering × Business Operations**

---

<div align="center">

<a href="https://aparnapradhanportfolio.netlify.app/" target="_blank">
<img src="https://img.shields.io/badge/Portfolio-Case_Studies-111111?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio" />
</a>
&nbsp;
<a href="https://www.linkedin.com/in/aparna-pradhan-06b882215/" target="_blank">
<img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
</a>
&nbsp;
<a href="mailto:softservicesinc.portfolio@gmail.com">
<img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
</a>

</div>

---

## What I Build

I am particularly interested in AI systems that have to operate **inside existing business processes**, rather than isolated chat interfaces.

That means dealing with:

* messy and heterogeneous data
* APIs and enterprise systems
* legacy infrastructure
* ambiguous operational cases
* business rules and policy
* human approval
* failure and recovery
* security and authorization
* evaluation and regression
* measurable operational outcomes

My current work explores this through three different problem classes.

---

# Engineering Philosophy

> **AI handles ambiguity. Deterministic software handles truth, authority, and execution.**

LLMs are powerful reasoning components, but they should not automatically become the system of record, authorization layer, or source of truth.

I therefore design around explicit boundaries:

| Principle                  | What it means                                                   |
| -------------------------- | --------------------------------------------------------------- |
| **Bounded agents**         | Explicit tools, permissions, context, budgets, and state        |
| **Deterministic controls** | Validation, business rules, reconciliation, authorization       |
| **Evidence**               | Important claims should be traceable to their source            |
| **Human oversight**        | Humans retain authority where automation is unsafe or ambiguous |
| **Verification**           | Actions are independently verified rather than trusted blindly  |
| **Evaluation**             | Golden cases, regression tests, adversarial scenarios           |
| **Observability**          | Workflow state, traces, errors, latency, and AI telemetry       |
| **Failure-first design**   | Retries, idempotency, timeouts, stale state, partial failure    |

The objective is not to make an AI system *look autonomous*.

It is to make it **useful, bounded, observable, and reliable enough to participate in real operational workflows.**

---

# Current Projects

## 01 · FinSight

### AI-assisted Financial Resolution

[**View Repository →**](https://github.com/Aparnap2/Finsight)

FinSight is a focused financial-resolution system modeled around a single B2B commerce company.

Its job is to:

> **Detect → Investigate → Explain → Propose → Authorize → Execute → Verify → Close**

The system reasons across heterogeneous financial systems including:

* payment-provider state
* accounting records
* expected settlement data
* email and collaboration context
* a legacy COBOL-style settlement boundary

### Architecture

```text
                Financial Systems
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
    Payments       Accounting      Legacy
        │              │              │
        └──────────────┼──────────────┘
                       ▼
              Deterministic Core
          Reconciliation · Evidence
             Rules · State · Policy
                       │
                       ▼
                AI Investigator
             Reason · Correlate
                 · Explain
                 · Propose
                       │
                       ▼
                Human / Policy
                    Gate
                       │
                       ▼
                   Execute
                       │
                       ▼
              Independent Verify
                       │
                       ▼
                     Close
```

### Core boundary

**The agent can:**

* investigate
* gather evidence
* generate hypotheses
* correlate information
* explain discrepancies
* propose resolutions

**The agent cannot:**

* establish financial truth
* authorize its own action
* bypass policy
* execute arbitrary operations
* verify its own execution

Current engineering work includes:

* deterministic financial reconciliation
* evidence-backed investigation
* typed agent capabilities
* authority boundaries
* human resolution workflows
* legacy batch integration
* idempotent execution
* adversarial evaluation
* security and isolation
* post-execution verification

**Status:** Active development

---

# 02 · ClaimOps AI

### Evidence-Driven AI for Health-Insurance Claims Operations

[**View Repository →**](https://github.com/Aparnap2/Claim_Ops)

ClaimOps explores how AI can assist claims operations while keeping adjudication authority with the insurer or TPA.

The core workflow:

```text
Claim
  ↓
Document Ingestion
  ↓
Classification / Extraction
  ↓
Evidence & Provenance
  ↓
Deterministic Validation
  ↓
Exception
  ↓
Bounded Investigation
  ↓
Evidence-Grounded Finding
  ↓
Human Review
  ↓
Audit
```

### AI is used for cognitive work

* interpreting heterogeneous documents
* investigating ambiguous exceptions
* gathering relevant evidence
* forming hypotheses
* preparing findings

### Deterministic software controls

* validation
* state transitions
* authorization
* evidence verification
* workflow execution
* auditability

The system is deliberately positioned **beside** the insurer's adjudication process rather than replacing it.

Current engineering work includes:

* evidence-grounded agent tools
* deterministic-first orchestration
* durable workflow state
* failure and retry semantics
* tenant isolation
* adversarial testing
* evaluation harnesses
* observability
* human-review routing

**Status:** Active development

---

# 03 · OntologyAI

### Business Discovery → Ontology → Workflow → Solution Design

[**View Repository →**](https://github.com/Aparnap2/Ontology_AI)

OntologyAI explores the problem that comes **before** implementation:

> **How do you turn messy business context into a structured understanding of an organization, its processes, systems, and operational problems?**

The core idea:

```text
Business Context
       ↓
Domain Model
       ↓
Entities & Relationships
       ↓
Processes
       ↓
Operational Pain Points
       ↓
Solution Design
```

It focuses on the discovery and solution-design side of enterprise AI engineering.

**Status:** Experimental / evolving

---

# The Common Thread

These projects are intentionally different.

They explore different business problems, data shapes, system constraints, and risk models.

But they share the same engineering principle:

```text
Business Problem
       ↓
Workflow Understanding
       ↓
System & Data Mapping
       ↓
Deterministic Controls
       ↓
Bounded AI
       ↓
Human / Policy Boundary
       ↓
Execution
       ↓
Verification
       ↓
Observable Outcome
```

I am interested in **where AI belongs inside a system — and equally, where it should not be trusted.**

---

# Engineering Focus

### Applied AI

`Python` · `FastAPI` · `LangGraph` · `LLM APIs` · `RAG` · `Tool Calling` · `Structured Outputs` · `Context Engineering` · `Agent Evaluation`

### Backend & Data

`PostgreSQL` · `Redis` · `Pydantic` · `AsyncIO` · `REST APIs` · `Webhooks` · `SQL` · `Schema Mapping` · `Data Reconciliation`

### Enterprise Integration

`APIs` · `Events` · `Queues` · `Batch Processing` · `Object Storage` · `Legacy Systems` · `Canonical Models` · `Idempotency`

### Reliability & Security

`TDD` · `CI/CD` · `Observability` · `OpenTelemetry` · `Auditability` · `RBAC` · `Isolation` · `Prompt-Injection Defense` · `Failure Testing`

### Cloud & Infrastructure

`AWS` · `GCP` · `Docker` · `Linux`

---

# How I Engineer

I prefer an evidence-driven development loop:

```text
Specification
     ↓
Contract
     ↓
RED Tests
     ↓
Implementation
     ↓
GREEN
     ↓
Integration Testing
     ↓
Adversarial Testing
     ↓
Review
     ↓
PR
     ↓
Merge
     ↓
Evidence
```

A system is not complete because the happy path works.

I want to understand:

* What happens when data is malformed?
* What happens when the model is wrong?
* What happens when a tool fails?
* What happens when a request is duplicated?
* What happens when evidence is missing?
* What happens when state becomes stale?
* What happens when an external dependency disappears?
* What prevents an agent from exceeding its authority?

---

# What I'm Working Toward

I am developing toward roles at the intersection of:

**Applied AI · Agent Engineering · AI Solutions · Enterprise Integration · Forward-Deployed Engineering**

I enjoy problems where the work starts with an ambiguous business process and ends with a working technical system:

```text
Understand the business
        ↓
Map the workflow
        ↓
Understand the data
        ↓
Identify the real constraint
        ↓
Design the solution
        ↓
Build the system
        ↓
Integrate with existing infrastructure
        ↓
Evaluate it
        ↓
Deploy and observe it
        ↓
Measure the outcome
```

---

## Beyond the Code

I am particularly interested in the question:

> **How do we make AI useful inside real organizations without pretending that probabilistic models are deterministic systems?**

That's the engineering problem I'm exploring.

---

<div align="center">

### Let's build systems, not just demos.

<br/>

<a href="https://aparnapradhanportfolio.netlify.app/">Portfolio</a>
  ·   <a href="https://www.linkedin.com/in/aparna-pradhan-06b882215/">LinkedIn</a>
  ·   <a href="mailto:softservicesinc.portfolio@gmail.com">Email</a>

<br/><br/>

<sub>Applied AI · Agentic Systems · Enterprise Integration · Reliable Software</sub>

</div>


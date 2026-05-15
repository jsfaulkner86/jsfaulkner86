<h1 align="center">John Faulkner</h1>

<p align="center">
  <strong>Agentic Healthcare AI Architect</strong><br/>
  Translating enterprise clinical workflow patterns into inspectable, governed, production-grade agentic AI systems.
</p>

<p align="center">
  <a href="https://thefaulknergroupadvisors.com">The Faulkner Group</a> ·
  <a href="https://linkedin.com/in/johnathonfaulkner">LinkedIn</a> ·
  Healthcare Workflow Systems ·
  Epic EHR to Agentic AI
</p>

---

## Architecture thesis

I design agentic AI systems for healthcare workflows where trust, traceability, escalation, and operational fit matter.

My work translates production Epic-era automation patterns into modern agent architectures: objective normalizers, planners, tool routers, FHIR/EHR interfaces, RAG pipelines, clinical safety verifiers, human approval paths, audit logs, and evaluation harnesses.

These are not demo agents. They are healthcare workflow systems designed around PHI boundaries, clinical risk, governance, observability, and operational handoff.

---

## Agentic healthcare system spine

```mermaid
%%{init: {
  "theme": "base",
  "themeVariables": {
    "background": "#111418",
    "primaryColor": "#161B22",
    "primaryTextColor": "#E6EDF3",
    "primaryBorderColor": "#2F817D",
    "lineColor": "#C7A74A",
    "secondaryColor": "#1D232B",
    "tertiaryColor": "#111418",
    "fontFamily": "Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif"
  }
}}%%

flowchart LR
    A[Clinical Workflow Request] --> B[Objective Normalizer]
    B --> C[Planner]
    C --> D[Tool Router]

    D --> E[FHIR APIs]
    D --> F[EHR Workflow Context]
    D --> G[Clinical RAG]
    D --> H[Simulation Sandbox]

    E --> I[Verifier Layer]
    F --> I
    G --> I
    H --> I

    I --> J[Human Escalation]
    I --> K[Policy Check]
    I --> L[Evaluation Harness]

    J --> M[Auditable Output]
    K --> M
    L --> M

    M --> N[Audit Log]
    M --> O[Telemetry]
    M --> P[Replay and Drift Monitoring]
```

---

## Production background

- **14 years** designing enterprise healthcare workflow systems in Epic environments
- **12 Tier 1 health system deployments**
- **50,000-user production environments**
- **40+ Epic upgrades and implementations**
- **17,000 births/year** coordinated through automated clinical workflow design
- Clinical domains: maternal health, prior authorization, In-Basket routing, registry validation, transition-of-care documentation

---

## Open-source architecture portfolio

| Layer | Repository | What it demonstrates |
|---|---|---|
| Interoperability | [`ehr-mcp`](https://github.com/jsfaulkner86/ehr-mcp) | Framework-agnostic protocol thinking for multi-agent healthcare AI |
| Clinical workflow agents | [`clinical-triage-agent`](https://github.com/jsfaulkner86/clinical-triage-agent) | Epic In-Basket routing translated into LangGraph and PydanticAI |
| Women's health workflow systems | [`pph-risk-scoring-agent`](https://github.com/jsfaulkner86/pph-risk-scoring-agent) | Stateful escalation logic for postpartum hemorrhage risk |
| Prior authorization | [`prior-auth-research-agent`](https://github.com/jsfaulkner86/prior-auth-research-agent) | CrewAI and RAG applied to one of healthcare's most broken workflows |
| Governance and safety | [`healthcare-compliance-guardrail`](https://github.com/jsfaulkner86/healthcare-compliance-guardrail) | PHI-aware guardrails, policy checks, approval boundaries, and compliance middleware |
| Clinical knowledge retrieval | [`clinical-rag-agent`](https://github.com/jsfaulkner86/clinical-rag-agent) | Clinical guideline retrieval architecture for point-of-care support |

---

## Architecture patterns I build around

| Pattern | Healthcare use case | Design concern |
|---|---|---|
| Objective normalization | Turning ambiguous clinical or operational requests into structured goals, constraints, and policies | Prevents agents from acting on vague or unsafe instructions |
| Planner plus task graph | Decomposing multi-step healthcare workflows into observable, interruptible steps | Supports review, replay, and operational handoff |
| Tool routing | Calling EHR, FHIR, RAG, document, scheduling, analytics, and workflow systems through governed interfaces | Keeps autonomy bounded by explicit tool contracts |
| Verifier layer | Checking clinical safety, PHI handling, policy fit, and output quality before action | Reduces unsafe automation and hallucinated workflow execution |
| Human escalation | Routing uncertain, high-risk, or policy-sensitive decisions to accountable humans | Keeps clinical accountability intact |
| Evaluation harness | Testing agents against known workflow cases, edge conditions, latency targets, and failure modes | Makes quality measurable before deployment |
| Audit and replay | Capturing plans, tool calls, intermediate state, approvals, and outputs | Enables governance, incident review, and continuous improvement |

---

## Design principles

- **Start with workflow, not model choice.** The agent architecture should reflect the operational pathway, exception handling, and human escalation model.
- **Make every agent inspectable.** Plans, tool calls, intermediate state, policy decisions, and outputs should be traceable and replayable.
- **Govern before autonomy.** Healthcare agents need approval thresholds, PHI boundaries, kill switches, audit trails, and role-based escalation.
- **Evaluate against clinical risk.** Accuracy alone is not enough. Evaluation should include safety, latency, drift, equity, and failure-mode analysis.
- **Use agents only where agents are warranted.** If a deterministic workflow, rules engine, or single LLM call with tools is enough, do not create a multi-agent system.

---

## Current focus

I am building reference implementations for agentic healthcare workflows across:

- Epic-style clinical task routing
- Prior authorization research and evidence assembly
- Maternal health risk escalation
- Healthcare compliance guardrails
- FHIR and EHR interoperability patterns
- Agent evaluation, governance, and auditability

---

## Technical stack

| Area | Tools and patterns |
|---|---|
| Agent orchestration | LangGraph, LangChain, CrewAI, PydanticAI, AutoGen |
| Healthcare interoperability | Epic workflow patterns, FHIR, HL7, EHR integration design |
| Retrieval and knowledge systems | RAG, vector stores, Chroma, Pinecone, pgvector |
| Backend systems | Python, FastAPI, TypeScript, Node.js |
| Evaluation and observability | pytest, LangSmith-style tracing, policy checks, audit logs, replayable workflows |
| Governance | PHI boundaries, role-based approvals, escalation paths, clinical safety review, compliance guardrails |

---

## Healthcare workflow translation

| Production healthcare pattern | Agentic AI system equivalent |
|---|---|
| Epic In-Basket routing | Clinical task triage agent with prioritization, routing, and escalation |
| PPH risk scoring | Stateful risk agent with rule evaluation, thresholding, and human review |
| Prior authorization research | Evidence assembly agent using RAG, payer policy retrieval, and document generation |
| Pregnancy registry validation | Rule and exception-handling loop with structured verification |
| Transition-of-care documentation | Multi-source RAG pipeline with auditable document assembly |

---

## Background

I am the CEO and Co-Founder of [The Faulkner Group](https://thefaulknergroupadvisors.com), a healthcare AI advisory firm focused on women's health technology, clinical workflow architecture, and AI-native operating models.

Before building open-source healthcare agents, I spent more than a decade designing and supporting enterprise Epic workflows in production environments where reliability, governance, and operational adoption were not optional.

This GitHub profile is where I codify those healthcare workflow patterns into agentic AI reference architectures, prototypes, and implementation playbooks.

---

## Connect

| Channel | Link |
|---|---|
| Website | [thefaulknergroupadvisors.com](https://thefaulknergroupadvisors.com) |
| LinkedIn | [linkedin.com/in/johnathonfaulkner](https://linkedin.com/in/johnathonfaulkner) |
| GitHub | [github.com/jsfaulkner86](https://github.com/jsfaulkner86) |


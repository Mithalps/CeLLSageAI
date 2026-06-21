# CellSage AI

### Agentic Copilot for EV Battery Manufacturing Root Cause Analysis

[![Status](https://img.shields.io/badge/status-hackathon--submission-blue?style=flat-square)]()
[![Frontend](https://img.shields.io/badge/frontend-React%20%2B%20TypeScript-3B82F6?style=flat-square&logo=react&logoColor=white)]()
[![Backend](https://img.shields.io/badge/backend-FastAPI-22C55E?style=flat-square&logo=fastapi&logoColor=white)]()
[![Orchestration](https://img.shields.io/badge/orchestration-LangGraph-8B5CF6?style=flat-square)]()
[![Inference](https://img.shields.io/badge/inference-Groq%20LLM-EF4444?style=flat-square)]()
[![Vector DB](https://img.shields.io/badge/vector%20db-ChromaDB-F59E0B?style=flat-square)]()
[![License](https://img.shields.io/badge/license-MIT-6B7280?style=flat-square)]()

> **Root cause analysis for battery manufacturing failures, compressed from hours to minutes — with evidence, not guesses.**

---

## Table of Contents

- [Demo](#demo)
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Core Innovation](#core-innovation)
- [Tech Stack](#tech-stack)
- [Frontend Features](#frontend-features)
- [Backend Features](#backend-features)
- [Multi-Agent Architecture](#multi-agent-architecture)
- [RAG Pipeline](#rag-pipeline)
- [System Architecture](#system-architecture)
- [Investigation Workflow](#investigation-workflow)
- [Datasets](#datasets)
- [Product Showcase](#product-showcase)
- [Quick Navigation](#quick-navigation)
- [Local Setup](#local-setup)
- [Future Roadmap](#future-roadmap)
- [Why CellSage AI Matters](#why-cellsage-ai-matters)
- [Why CellSage AI Stands Out](#why-cellsage-ai-stands-out)
- [Team Contributions](#team-contributions)
- [Conclusion](#conclusion)

---

## Demo

<div align="center">

[![Working Demo Video](https://img.shields.io/badge/🎥_Working_Demo-YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtu.be/Xjzm5axWjEs)
[![Live Demo](https://img.shields.io/badge/🌐_Live_Demo-Visit_App-3B82F6?style=for-the-badge)](#)
[![GitHub Repository](https://img.shields.io/badge/💻_GitHub-Repository-181717?style=for-the-badge&logo=github&logoColor=white)](#)
[![Presentation Deck](https://img.shields.io/badge/📑_Presentation-Deck-F59E0B?style=for-the-badge)](#)
[![Architecture Overview](https://img.shields.io/badge/🏗️_Architecture-Overview-8B5CF6?style=for-the-badge)](#system-architecture)

</div>

> *Links above are placeholders — swap in the live deployment, repository, and deck URLs once available.*

---

## Overview

**CellSage AI** is an AI-powered manufacturing intelligence platform that accelerates **Root Cause Analysis (RCA)** for EV battery production environments.

It fuses **agentic AI workflows**, **Retrieval-Augmented Generation (RAG)**, **manufacturing knowledge retrieval**, **historical incident intelligence**, and **automated investigation reporting** into a single system — enabling engineers to move from "we have a defect" to "here is the root cause and the corrective action" in minutes rather than days.

CellSage AI isn't a chatbot bolted onto a knowledge base. It's a structured, multi-agent investigation pipeline purpose-built to reason the way an experienced manufacturing engineer does: gather evidence first, reason second, recommend third — every conclusion traceable back to a source.

---

## Problem Statement

Modern EV battery manufacturing generates large volumes of fragmented operational data spread across disconnected systems:

| Data Source | Examples |
|---|---|
| Process Documentation | SOPs, work instructions, quality manuals |
| Maintenance Systems | Equipment logs, calibration records |
| Historical Records | Past failure reports, deviation logs |
| Sensor Telemetry | Line sensor readings, process parameters |
| Production Systems | Batch records, yield data |

When a failure occurs — a thermal runaway event, an electrolyte leak, a capacity fade outlier — engineers must manually cross-reference all of these sources to piece together a root cause. This manual correlation process leads to:

- **Slow root cause analysis** — investigations stretch from hours into days
- **Increased downtime** — production lines stay halted longer than necessary
- **Higher scrap rates** — delayed fixes mean more defective cells produced
- **Reduced manufacturing efficiency** — engineering hours consumed by data archaeology instead of problem-solving
- **Knowledge silos** — tribal knowledge trapped in the heads of senior engineers, not systematized

**CellSage AI solves this through autonomous evidence retrieval and multi-agent reasoning** — turning scattered manufacturing data into a structured, explainable investigation in real time.

---

## Core Innovation

The key innovation behind CellSage AI is an **Agentic AI Investigation Pipeline** that mirrors the cognitive workflow of an experienced manufacturing engineer conducting a failure investigation.

Rather than returning a single LLM-generated answer to a query, CellSage AI executes a structured reasoning sequence:

1. **Retrieves evidence** — pulls relevant SOPs, historical failures, and maintenance records via semantic search
2. **Analyzes manufacturing context** — interprets sensor and process data tied to the reported issue
3. **Identifies root causes** — synthesizes retrieved evidence into a ranked set of probable causes
4. **Evaluates confidence** — scores each hypothesis based on evidence strength and historical precedent
5. **Generates corrective actions** — proposes actionable, SOP-aligned remediation steps
6. **Produces structured investigation reports** — compiles the full investigation into an exportable, audit-ready document

This sequential, agent-driven approach is what separates CellSage AI from a generic RAG chatbot: every output is **traceable, evidence-backed, and structured for real engineering decision-making**.

---

## Tech Stack

### Frontend
- **React** — component-driven UI
- **TypeScript** — type-safe application logic
- **Vite** — fast build tooling and dev server
- **Tailwind CSS** — utility-first styling for the industrial dark theme
- **Axios** — API communication layer
- **Recharts** — interactive analytics visualizations
- **Lucide Icons** — consistent, modern iconography

### Backend
- **FastAPI** — high-performance async API layer
- **Python** — core backend runtime

### AI Layer
- **LangGraph** — agentic orchestration and state-machine workflow control
- **LangChain** — LLM tooling and chaining utilities
- **Groq LLM** — low-latency inference engine powering agent reasoning

### Knowledge Layer
- **ChromaDB** — vector database for semantic document retrieval
- **SQLite** — structured storage for investigation history and metadata

### Data Sources
- SOP Documents
- Historical Failure Cases
- Maintenance Records
- Manufacturing Sensor Logs

---

## Frontend Features

### 1. Landing Page
A polished, enterprise-grade entry point that communicates the product's value proposition at a glance — built with an industrial dark theme suited to a manufacturing operations audience rather than a generic SaaS aesthetic.

### 2. Investigation Workspace
The core working surface where engineers describe an issue and watch the multi-agent pipeline execute in real time — evidence retrieval, sensor analysis, and root cause reasoning are surfaced as the investigation progresses, not hidden behind a spinner.

### 3. Executive Dashboard
A high-level operational view summarizing investigation volume, recurring failure categories, and resolution trends — designed for plant managers and engineering leads who need the summary, not the raw transcript.

### 4. Historical Investigation Explorer
A searchable archive of past investigations, enabling engineers to surface prior cases with similar symptoms before starting a new investigation from scratch — turning tribal knowledge into a queryable asset.

### 5. Analytics Dashboard
Interactive charts (via Recharts) visualizing failure trends, root cause distribution, and investigation turnaround time — giving teams a quantitative view of manufacturing reliability over time.

### 6. Investigation Report Generator
Automatically compiles the full investigation — evidence, reasoning trail, root cause, and recommendations — into a structured, shareable report.

### 7. PDF Export Capability
One-click export of any investigation report to a clean, audit-ready PDF for quality documentation, compliance records, or stakeholder distribution.

**Design highlights:**
- Enterprise-grade dark theme tuned for industrial/manufacturing operations contexts
- Industrial analytics UI with high information density and minimal visual noise
- Real-time investigation workflow visualization as agents execute
- Interactive, drillable charts across all dashboards
- Fast, searchable investigation history

---

## Backend Features

CellSage AI's backend is built on **FastAPI**, chosen for its async-first design, automatic OpenAPI documentation, and strong typing support — all critical for an API layer coordinating multiple AI agents under real-time constraints.

The backend is organized into four functional API groups:

- **Investigation APIs** — create, track, and manage the lifecycle of an investigation from submission to resolution
- **Retrieval APIs** — expose direct semantic search over the knowledge base for evidence lookup
- **Report APIs** — generate, retrieve, and export structured investigation reports
- **Investigation History APIs** — query and filter past investigations for the Historical Investigation Explorer

### Endpoint Overview

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/investigations` | Submit a new manufacturing issue and trigger the agent pipeline |
| `GET` | `/api/investigations/{id}` | Retrieve the full state and results of a specific investigation |
| `GET` | `/api/investigations` | List and filter historical investigations |
| `POST` | `/api/retrieval/query` | Run a direct semantic search against the knowledge base |
| `GET` | `/api/reports/{id}` | Retrieve the structured report for an investigation |
| `GET` | `/api/reports/{id}/export` | Export an investigation report as PDF |
| `GET` | `/api/analytics/summary` | Fetch aggregated metrics for the Executive Dashboard |
| `GET` | `/api/health` | Service health check |

---

## Multi-Agent Architecture

CellSage AI's reasoning engine is composed of four specialized agents, orchestrated via **LangGraph** as a coordinated state machine rather than a single monolithic prompt.

### 1. Retrieval Agent
Responsible for semantic search across the knowledge layer — querying ChromaDB to surface the most relevant SOPs, historical failure cases, and maintenance records for the reported issue. This agent grounds the entire investigation in real evidence before any reasoning takes place.

### 2. Sensor Analysis Agent
Interprets manufacturing sensor and process telemetry tied to the reported issue, identifying anomalies, threshold deviations, and patterns that correlate with known failure signatures.

### 3. Root Cause Agent
Synthesizes the outputs of the Retrieval and Sensor Analysis agents into a ranked set of probable root causes, each annotated with a confidence score derived from evidence strength and historical precedent.

### 4. Recommendation Agent
Translates the identified root cause(s) into concrete, SOP-aligned corrective actions — ensuring recommendations are not generic advice but grounded in the organization's own documented procedures.

Each agent operates on a shared investigation state, passing structured outputs downstream — making the entire reasoning chain inspectable and auditable, rather than a black box.

---

## RAG Pipeline

CellSage AI's retrieval system is what keeps every agent output grounded in real manufacturing evidence rather than LLM speculation.

### Flow

```
User Query
    │
    ▼
ChromaDB Retrieval (vector similarity search)
    │
    ▼
Top-K Relevant Documents
    │
    ▼
Context Construction (evidence assembly + metadata tagging)
    │
    ▼
LLM Reasoning (Groq)
    │
    ▼
Evidence-Backed Response
```

### How it works

- **Vector embeddings** — SOPs, historical failure cases, and maintenance records are embedded and indexed in ChromaDB, enabling semantic (meaning-based) rather than keyword-based search
- **Semantic search** — queries are embedded using the same model and matched against the document index via cosine similarity
- **Similarity retrieval** — the top-K most relevant documents are retrieved for each query, ranked by relevance score
- **Source attribution** — every piece of evidence used in an agent's reasoning is tagged with its originating document, so investigation conclusions can always be traced back to a specific SOP, log, or historical case

This pipeline ensures CellSage AI never answers from memory alone — every claim has a citable source.

---

## System Architecture

```mermaid
flowchart TD
    User(["👤 User"])

    subgraph FE["FRONTEND LAYER"]
        direction TB
        Frontend["React + TypeScript<br/>Vite · Tailwind CSS"]
    end

    subgraph BE["API LAYER"]
        direction TB
        Backend["FastAPI Backend<br/>Investigation · Retrieval · Report APIs"]
    end

    subgraph ORCH["ORCHESTRATION LAYER"]
        direction TB
        LangGraph["LangGraph Orchestrator<br/>Multi-Agent State Machine"]
    end

    subgraph AGENTS["AGENT LAYER"]
        direction LR
        A1["Retrieval<br/>Agent"]
        A2["Sensor Analysis<br/>Agent"]
        A3["Root Cause<br/>Agent"]
        A4["Recommendation<br/>Agent"]
    end

    subgraph KNOW["KNOWLEDGE + REASONING LAYER"]
        direction LR
        Chroma[("ChromaDB<br/>Vector Database")]
        Groq["Groq LLM<br/>Inference Engine"]
        SQLite[("SQLite<br/>Investigation History")]
    end

    Report(["📄 Investigation Report"])

    User --> Frontend
    Frontend -- "REST / Axios" --> Backend
    Backend --> LangGraph
    LangGraph --> A1 & A2 & A3 & A4
    A1 --> Chroma
    A2 --> Groq
    A3 --> Groq
    A4 --> Groq
    Chroma --> Groq
    Groq --> SQLite
    SQLite --> Report

    classDef frontend fill:#3B82F6,stroke:#1E40AF,stroke-width:2px,color:#ffffff,font-weight:bold
    classDef backend fill:#22C55E,stroke:#15803D,stroke-width:2px,color:#ffffff,font-weight:bold
    classDef agent fill:#8B5CF6,stroke:#5B21B6,stroke-width:2px,color:#ffffff,font-weight:bold
    classDef chroma fill:#F59E0B,stroke:#B45309,stroke-width:2px,color:#ffffff,font-weight:bold
    classDef groq fill:#EF4444,stroke:#B91C1C,stroke-width:2px,color:#ffffff,font-weight:bold
    classDef sqlite fill:#6B7280,stroke:#374151,stroke-width:2px,color:#ffffff,font-weight:bold
    classDef endpoint fill:#111827,stroke:#374151,stroke-width:2px,color:#ffffff,font-weight:bold
    classDef subgraphStyle fill:#0F172A,stroke:#1E293B,stroke-width:1px,color:#94A3B8

    class Frontend frontend
    class Backend backend
    class LangGraph backend
    class A1,A2,A3,A4 agent
    class Chroma chroma
    class Groq groq
    class SQLite sqlite
    class User,Report endpoint
    class FE,BE,ORCH,AGENTS,KNOW subgraphStyle
```

### How Data Flows Through the Platform

A request enters through the **React + TypeScript frontend**, where an engineer submits a manufacturing issue. The **FastAPI backend** receives the request and hands it to the **LangGraph Orchestrator**, which drives the investigation as a coordinated state machine rather than a single LLM call.

The orchestrator dispatches the **Retrieval, Sensor Analysis, Root Cause, and Recommendation agents**, each contributing a distinct piece of the investigation. The Retrieval Agent pulls grounding evidence from **ChromaDB**; all four agents reason over that evidence using the **Groq LLM** for low-latency inference. Every output — evidence, reasoning trail, root cause, recommendation — is persisted in **SQLite**, which feeds both the Historical Investigation Explorer and the final **Investigation Report** returned to the user.

The result is a closed loop: every investigation is evidence-grounded going in, and fully auditable coming out.

---

## Investigation Workflow

CellSage AI models the full lifecycle of a manufacturing investigation, end to end:

1. **User submits issue** — an engineer describes the failure (e.g., "Cell batch B-2207 showing elevated internal resistance post-formation")
2. **Evidence retrieval** — the Retrieval Agent queries ChromaDB for relevant SOPs and historical precedent
3. **Sensor analysis** — the Sensor Analysis Agent inspects associated process telemetry for anomalies
4. **Root cause reasoning** — the Root Cause Agent synthesizes evidence into ranked, confidence-scored hypotheses
5. **Recommendation generation** — the Recommendation Agent proposes SOP-aligned corrective actions
6. **Report generation** — the full investigation trail is compiled into a structured, exportable report

Each stage is surfaced live in the Investigation Workspace, so the engineer sees the reasoning unfold — not just a final answer.

---

## Datasets

To demonstrate the platform's reasoning capability without relying on proprietary manufacturing data, CellSage AI ships with a curated **synthetic manufacturing dataset**, modeled on realistic EV battery production scenarios:

- **10 SOPs** — covering formation, electrode coating, cell assembly, and quality inspection procedures
- **20 Historical Failure Cases** — spanning thermal, electrical, and mechanical failure modes with documented root causes and resolutions
- **10 Maintenance Records** — equipment calibration and service logs correlated with several of the historical failure cases

These datasets were purpose-built to:

- Demonstrate realistic cross-referencing between SOPs, failures, and maintenance history
- Allow the agent pipeline to be evaluated against known ground-truth root causes
- Avoid reliance on confidential or proprietary manufacturing data while still reflecting authentic industry scenarios

---

## Product Showcase

### Executive Dashboard

![Executive Dashboard](./Screenshots/dashboard.png)

The Executive Dashboard distills weeks of investigation activity into a single operational view — open investigations, recurring failure categories, and resolution velocity, all visible at a glance. Plant managers and engineering leads get the signal they need to prioritize without digging through individual case files, turning CellSage AI from an engineering tool into a decision-making instrument for production leadership.

### Analytics Dashboard

![Analytics Dashboard](./Screenshots/analytics.png)

Built on interactive, drillable charts, the Analytics Dashboard surfaces failure trends, root cause distribution, and investigation turnaround time across the full manufacturing history. Engineers can spot a failure mode trending upward across batches before it escalates into a line-wide quality event — shifting the team from reactive troubleshooting to proactive pattern recognition.

### Investigation History

![Investigation History](./Screenshots/history.png)

Every past investigation becomes a searchable, reusable asset rather than a closed ticket. Engineers facing a new failure can instantly surface prior cases with matching symptoms, root causes, or affected equipment — cutting redundant diagnostic work and preserving institutional knowledge that would otherwise leave with senior staff.

### Investigation Report

![Investigation Report](./Screenshots/report.png)

Each investigation concludes in a structured, audit-ready report — full evidence trail, confidence-scored root cause, and SOP-aligned corrective actions, exportable to PDF in one click. This is the artifact that extends CellSage AI's value beyond the engineering team, into quality reviews, compliance audits, and stakeholder updates.

---

## Quick Navigation

```
CellSageAI/
│
├── backend/                 # FastAPI services, agents, RAG pipeline
├── src/                     # React + TypeScript application source
├── public/                  # Static public assets
├── Screenshots/             # Product screenshots
├── docs/                    # Architecture notes & supporting documentation
├── README.md
├── package.json
├── vite.config.ts
├── tsconfig.json
└── configuration files
```

| | |
|---|---|
|  **Source Code** | [`./src`](./src) |
|  **Backend Services** | [`./backend`](./backend) |
|  **Screenshots** | [`./Screenshots`](./Screenshots) |
|  **Documentation** | [`./docs`](./docs) |
|  **Public Assets** | [`./public`](./public) |

---

## Local Setup

### Prerequisites
- Python 3.10+
- Node.js 18+
- A Groq API key

### Backend

```bash
cd backend
pip install -r requirements.txt
py -m uvicorn main:app --reload
```

The backend will be available at `http://localhost:8000`, with interactive API docs at `http://localhost:8000/docs`.

### Frontend

```bash
npm install
npm run dev
```

The frontend will be available at `http://localhost:5173`.

> Ensure backend environment variables (Groq API key, ChromaDB path, SQLite path) are configured in `backend/.env` before starting the server.

---

## Future Roadmap

CellSage AI is architected to extend well beyond its hackathon scope into a production-grade manufacturing intelligence platform:

- **Real-time MES integration** — live data ingestion from Manufacturing Execution Systems
- **ERP integration** — connecting investigation outcomes to procurement, inventory, and supply chain systems
- **Predictive maintenance** — shifting from reactive RCA to proactive failure prevention
- **IoT streaming** — real-time sensor ingestion for continuous anomaly detection
- **Digital twins** — simulating production lines to validate root cause hypotheses before physical intervention
- **Multi-factory deployment** — federated knowledge sharing across manufacturing sites
- **Explainable AI investigations** — deeper interpretability tooling so every agent decision is fully auditable by quality and compliance teams

---

## Why CellSage AI Matters

**From hours to minutes.** A typical battery failure investigation today means an engineer manually cross-referencing SOPs, maintenance logs, and historical cases — a process that routinely consumes several engineering hours per incident before a root cause is even confirmed. CellSage AI compresses that into a structured investigation that completes in minutes, freeing engineers to act on root causes instead of hunting for them.

**Decisions backed by evidence, not intuition.** Every root cause CellSage AI surfaces is tied to a specific SOP clause, sensor reading, or historical precedent — not an unsupported model guess. That traceability is what makes the output usable in a regulated manufacturing environment, where "the model said so" isn't an acceptable answer, but "here's the SOP section and the sensor log behind this" is.

**Manufacturing knowledge that doesn't walk out the door.** Process expertise tends to concentrate in a small number of senior engineers, and it leaves with them when they retire or move on. By systematizing historical investigations into a searchable, reasoning-capable knowledge base, CellSage AI converts tribal knowledge into an institutional asset that compounds in value over time instead of disappearing with attrition.

**Explainability as a requirement, not a feature.** In safety-critical manufacturing — where a missed root cause can mean a thermal event downstream — confidence scores and a visible reasoning trail aren't a UI flourish. They're what lets a quality team sign off on an AI-assisted investigation with the same rigor as a human-led one.

**Built to scale past one production line.** The same multi-agent architecture handling a single line today is designed to extend across MES integration, multiple factories, and predictive maintenance workflows without re-architecting the core reasoning pipeline.

**The bigger picture.** EV battery manufacturing is scaling globally faster than the supply of experienced RCA engineers. CellSage AI doesn't replace that expertise — it multiplies it, letting a smaller engineering team cover more production capacity without a proportional growth in investigation backlog.

---

## Why CellSage AI Stands Out

**Agentic AI architecture.** CellSage AI doesn't ask an LLM to "figure it out" in a single shot. It decomposes investigation into specialized agents — retrieval, sensor analysis, root cause reasoning, recommendation — each with a narrow, well-defined responsibility. This mirrors how real engineering teams actually investigate failures, and it produces more reliable, more inspectable results than a single-prompt chatbot ever could.

**RAG-powered manufacturing intelligence.** Every agent conclusion is grounded in retrieved evidence — SOPs, historical cases, maintenance records — not LLM speculation. This is the difference between a tool engineers can trust with real production decisions and a novelty demo.

**Explainable root cause analysis.** Confidence scores, source attribution, and a visible reasoning trail mean CellSage AI's outputs aren't a black box — they're auditable, which matters enormously in a regulated, safety-critical domain like EV battery manufacturing.

**Actionable recommendations.** Recommendations aren't generic LLM advice — they're tied directly to the organization's own SOPs, meaning what CellSage AI suggests is immediately executable on the shop floor.

**Enterprise deployment potential.** The architecture — FastAPI backend, vector-indexed knowledge layer, agent orchestration via LangGraph — is built to scale from a hackathon demo to a real multi-factory deployment, with a clear roadmap toward MES/ERP integration and predictive maintenance.

CellSage AI isn't a proof-of-concept chatbot wrapped in a battery-manufacturing theme. It's a domain-grounded, agentic reasoning system designed to solve one of the most expensive, time-consuming problems in EV manufacturing today.

---

## Conclusion

EV battery manufacturing sits at the intersection of precision engineering and massive scale — and the cost of a slow, fragmented investigation process compounds with every cell produced. **CellSage AI** reimagines root cause analysis not as a manual data-archaeology exercise, but as an autonomous, evidence-grounded reasoning process — one that gives engineers back their most valuable resource: time.

By combining agentic AI orchestration with retrieval-augmented manufacturing intelligence, CellSage AI points toward a future where every battery line failure is investigated with the speed of AI and the rigor of an expert engineer — at scale, across factories, and without losing institutional knowledge to attrition.

**CellSage AI reimagines root cause analysis through Agentic AI—combining retrieval, reasoning, and recommendation into a single intelligent investigation workflow.**

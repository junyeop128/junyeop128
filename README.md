<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,50:1E3A8A,100:2563EB&height=250&section=header&text=Junyeop%20Lee&fontSize=52&fontColor=FFFFFF&animation=fadeIn&fontAlignY=38&desc=Finance%20AI%20%7C%20RAGOps%20%7C%20Multi-Agent%20Systems%20%7C%20Deeptech%20Valuation&descAlignY=58&descSize=18)

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=21&duration=2600&pause=900&color=60A5FA&center=true&vCenter=true&width=950&lines=Building+AI+Workflows+for+Finance+and+Valuation;Designing+Evidence-based+RAG+and+RAGOps+Systems;Building+Multi-Agent+Decision+Support+Workflows;Connecting+Data%2C+Finance%2C+Evidence%2C+and+Evaluation)](https://git.io/typing-svg)

### Hi, I'm Junyeop Lee
### I build AI-driven workflows for finance, valuation, retrieval, and decision support.

<br/>

![GitHub followers](https://img.shields.io/github/followers/junyeop128?style=for-the-badge&logo=github&color=0F172A)
![GitHub User's stars](https://img.shields.io/github/stars/junyeop128?style=for-the-badge&logo=github&color=1E3A8A)

</div>

---

## 🚀 About Me

I am interested in **Finance AI**, **RAG / RAGOps**, **Deeptech Valuation**, **Multi-Agent Systems**, and **data-driven decision support**.

My work focuses on connecting **financial statements, policy and technology documents, market data, structured evidence, and AI workflows** to support valuation, investment review, credit/risk screening, retrieval-based reasoning, and decision support.

Rather than treating LLM output as the endpoint, I am especially interested in **evaluation-first AI systems**: systems that can trace evidence, measure retrieval quality, detect regressions, identify unsupported claims, and remain reproducible when models or data change.

<table>
<tr>
<td width="25%" align="center">

### 💰 Finance AI
Valuation  
Credit Screening  
Risk Review

</td>
<td width="25%" align="center">

### 🧠 AI Workflow
Multi-Agent Systems  
Decision Pipeline  
Human-in-the-loop

</td>
<td width="25%" align="center">

### 🔎 RAG / RAGOps
Evidence Retrieval  
Evaluation  
Regression Gates

</td>
<td width="25%" align="center">

### 📊 Data Analysis
Python · R · SQL  
Statistics · ML  
Business Analytics

</td>
</tr>
</table>

---

## 🧩 Featured Projects

<table>
<tr>
<td width="50%" valign="top">

### 🔎 [PolicyRAG Ops](https://github.com/junyeop128/PolicyRAG-Ops)

An evaluation-first RAG/RAGOps system for policy and finance documents.

**Validated highlights**

- Evidence-aware retrieval with parent vector + Evidence Unit signals
- Golden Dataset evaluation and retrieval regression gates
- Evidence readiness / promotion validation
- PostgreSQL + pgvector / HALFVEC 2048
- NVIDIA hosted embedding and grounded generation
- Docker / GitHub Actions / Terraform validation
- Hosted API failure diagnosis, retry, checkpoint/resume

**Post-freeze scale validation**

```text
167-page BOK report
530 parent chunks
9,172 Evidence Units
530 / 530 evidence coverage
```

| Metric | Vector | Vector + Evidence |
|---|---:|---:|
| Hit@3 | 0.857 | **1.000** |
| MRR | 0.889 | **0.929** |
| NDCG@5 | 0.916 | **0.947** |

Generation validation also measured citation validity, numeric faithfulness, abstention, and end-to-end latency.

[Open repository →](https://github.com/junyeop128/PolicyRAG-Ops)

</td>

<td width="50%" valign="top">

### 🧠 AlphaProve

A multi-agent AI framework for deeptech listed-company analysis, integrating finance, market, technology, issue, macro, chair, and auditor perspectives.

**Focus**

- Deeptech company analysis
- Financial / market / technology evidence integration
- Multi-agent decision pipeline
- Auditor / chair validation structure
- Valuation and investment-review support

**Keywords**

Finance AI · Multi-Agent · Valuation · Auditor · Chair · Deeptech

</td>
</tr>

<tr>
<td width="50%" valign="top">

### 📈 [DMA Valuation Evaluation](https://github.com/junyeop128/DMA-Valuation-evaluation)

A valuation and evaluation project connecting DMA-based signals, market data, backtesting logic, and investment decision-support interpretation.

**Keywords**

DMA · Valuation · Backtesting · Performance Evaluation · Investment Decision

[Open repository →](https://github.com/junyeop128/DMA-Valuation-evaluation)

</td>

<td width="50%" valign="top">

### 💼 JB Future Deal Screening AI

An AI-supported screening structure for credit review, investment review, facility finance, and portfolio-level decision support.

**Focus**

- Deal screening
- Credit / risk review
- Financial analysis
- Portfolio-level decision support
- Structured evidence packets

</td>
</tr>

<tr>
<td colspan="2" valign="top">

### 📥 Data Intake Agent

A structured data intake pipeline for collecting disclosures, financial statements, market data, and policy/rule-based evidence for downstream AI agents.

**Keywords**

OpenDART · Market Data · Policy Rules · Data Pipeline · Evidence · Structured Intake

</td>
</tr>
</table>

---

## 🔬 PolicyRAG Ops — What I Actually Validated

PolicyRAG Ops is the project where I most explicitly tested **retrieval quality, generation grounding, and operating failure modes**.

### Retrieval & Scale

- Frozen Hard Challenge: MRR **0.85 → 0.95**, Hit@1 **0.70 → 0.90**
- 167-page Bank of Korea report: **530 parent chunks / 9,172 Evidence Units**
- Scale retrieval: Hit@3 **0.857 → 1.000**, MRR **0.889 → 0.929**, NDCG@5 **0.916 → 0.947**
- Evidence coverage: **530 / 530**

### Generation & Evaluation

- Citation presence: **1.000**
- Citation validity: **1.000**
- Citation sentence coverage: **0.980**
- Numeric faithfulness: **0.956**
- Reference numeric recall: **1.000**
- Exact abstention: **1.000**

### Reliability / RAGOps

- Recovered a real hosted NVIDIA **502** with retry logic
- Added scale-test-only batch checkpoints / resumable embedding workflow
- Used PostgreSQL advisory lock to prevent duplicate runners
- Verified regression gate and promotion gate behavior
- Kept the existing primary DB unchanged during isolated scale validation

> These results are controlled local/hosted-API validation observations, not production traffic or SLA claims.

---

## 💡 Engineering Perspective

One result I care about: in the 167-page generation evaluation, an **LLM-as-judge scored correctness / groundedness / relevance at 1.000**, while a deterministic numeric evaluator still detected unsupported numeric claims in one answer.

That is why I prefer combining:

```text
LLM-based evaluation
        +
deterministic checks
        +
retrieval metrics
        +
lineage / regression gates
```

The goal is not only to make an AI answer well, but to build a system that can **detect when a plausible-looking answer is still unsupported**.

---

## 🛠 Core Skill Set

<table>
<tr>
<td width="50%" valign="top">

### 💼 Finance & Valuation

- Financial Statement Analysis
- Corporate / Industry Analysis
- Financial Modeling
- DCF & Sensitivity Analysis
- Peer Group Benchmarking
- Credit / Risk Review
- Investment Review
- Policy / Rule-based Screening

</td>

<td width="50%" valign="top">

### 🤖 AI & Decision Workflows

- Multi-Agent Workflow Design
- RAG / Vector Retrieval
- Evidence-based Report Generation
- JSON / Structured Packet Design
- Auditor / Chair Validation Logic
- Human-in-the-loop Decision Support
- LLM Evaluation
- Failure Analysis

</td>
</tr>

<tr>
<td width="50%" valign="top">

### 🔎 RAG / RAGOps

- Parent / Evidence Retrieval
- pgvector / HALFVEC
- Golden Dataset Evaluation
- MRR / Recall@K / Hit@K / NDCG@K
- Citation / Numeric Faithfulness
- Abstention Evaluation
- Regression / Promotion Gates
- Data & Embedding Lineage

</td>

<td width="50%" valign="top">

### ⚙️ Engineering & Data

- Python 3.12
- SQL / PostgreSQL
- FastAPI / SQLAlchemy
- Docker Compose
- Git / GitHub Actions
- Terraform validation
- NVIDIA NIM / Nemotron
- Pandas / NumPy / scikit-learn

</td>
</tr>
</table>

---

## 🧰 Selected Technologies

<div align="center">

![Python](https://img.shields.io/badge/Python-0F172A?style=for-the-badge&logo=python&logoColor=60A5FA)
![R](https://img.shields.io/badge/R-0F172A?style=for-the-badge&logo=r&logoColor=60A5FA)
![SQL](https://img.shields.io/badge/SQL-0F172A?style=for-the-badge&logo=postgresql&logoColor=60A5FA)
![Pandas](https://img.shields.io/badge/Pandas-0F172A?style=for-the-badge&logo=pandas&logoColor=8B5CF6)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-0F172A?style=for-the-badge&logo=scikitlearn&logoColor=F59E0B)

<br/>

![FastAPI](https://img.shields.io/badge/FastAPI-1E293B?style=for-the-badge&logo=fastapi&logoColor=22C55E)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1E293B?style=for-the-badge&logo=postgresql&logoColor=60A5FA)
![pgvector](https://img.shields.io/badge/pgvector-1E293B?style=for-the-badge&logo=postgresql&logoColor=8B5CF6)
![Docker](https://img.shields.io/badge/Docker-1E293B?style=for-the-badge&logo=docker&logoColor=60A5FA)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-1E293B?style=for-the-badge&logo=githubactions&logoColor=60A5FA)
![Terraform](https://img.shields.io/badge/Terraform-1E293B?style=for-the-badge&logo=terraform&logoColor=8B5CF6)

<br/>

![RAGOps](https://img.shields.io/badge/RAGOps-0F172A?style=for-the-badge)
![Golden Dataset](https://img.shields.io/badge/Golden%20Dataset-0F172A?style=for-the-badge)
![LLM Evaluation](https://img.shields.io/badge/LLM%20Evaluation-0F172A?style=for-the-badge)
![NVIDIA NIM](https://img.shields.io/badge/NVIDIA%20NIM-0F172A?style=for-the-badge&logo=nvidia&logoColor=76B900)
![LangChain](https://img.shields.io/badge/LangChain-0F172A?style=for-the-badge)
![LlamaIndex](https://img.shields.io/badge/LlamaIndex-0F172A?style=for-the-badge)

</div>

---

## 🎯 Current Interests

**Finance AI · Policy Finance · Credit / Risk Decision Support · Deeptech Valuation · RAG / RAGOps · Multi-Agent Systems · Reliable AI Evaluation**

I am especially interested in roles and projects where **financial / policy-domain reasoning** and **AI engineering** meet.

---

<div align="center">

### Building decision-support AI that connects data, evidence, evaluation, and domain reasoning.

</div>

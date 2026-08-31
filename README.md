<div align="center">

# Junyeop Lee

### Finance & Policy AI · RAG / RAGOps · Evidence-based Decision Systems

I build **evaluation-first AI systems** for policy and finance documents, with a focus on retrieval quality, grounded generation, reproducibility, and failure-aware operations.

[![PolicyRAG Ops](https://img.shields.io/badge/Featured-PolicyRAG%20Ops-2563EB?style=for-the-badge&logo=github&logoColor=white)](https://github.com/junyeop128/PolicyRAG-Ops)
[![Python](https://img.shields.io/badge/Python-3.12-0F172A?style=for-the-badge&logo=python&logoColor=60A5FA)](https://www.python.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-pgvector-0F172A?style=for-the-badge&logo=postgresql&logoColor=60A5FA)](https://github.com/pgvector/pgvector)
[![Docker](https://img.shields.io/badge/Docker-Validated-0F172A?style=for-the-badge&logo=docker&logoColor=60A5FA)](https://www.docker.com/)

</div>

---

## Featured Project — PolicyRAG Ops

**PolicyRAG Ops** is a RAG/RAGOps system for policy and finance documents that connects document processing, evidence-aware retrieval, grounded generation, Golden Dataset evaluation, regression gates, lineage, and promotion validation.

### What I validated

| Area | Result |
|---|---|
| **Frozen retrieval baseline** | Hard Challenge MRR **0.85 → 0.95**, Hit@1 **0.70 → 0.90** |
| **Post-freeze scale test** | 167-page BOK report → **530 parent chunks / 9,172 Evidence Units / 530/530 coverage** |
| **Scale retrieval** | Hit@3 **0.857 → 1.000**, MRR **0.889 → 0.929**, NDCG@5 **0.916 → 0.947** |
| **Scale generation** | Citation presence / validity **1.000**, numeric faithfulness **0.956**, exact abstention **1.000** |
| **Reliability** | Recovered a real hosted NVIDIA **502** with retry + batch checkpoints; resumable after interruption |
| **Safety of changes** | Regression gate + Evidence readiness + promotion gate; incomplete evidence snapshot blocked before mutation |

> Scale-test latency numbers are controlled observations from the local Lite + hosted API environment, **not production SLA claims**.

[Open PolicyRAG Ops →](https://github.com/junyeop128/PolicyRAG-Ops)

---

## Engineering Focus

<table>
<tr>
<td width="50%" valign="top">

### Retrieval & RAG

- Parent vector retrieval
- Evidence Unit MaxSim
- Character 3-gram evidence signal
- pgvector / HALFVEC 2048
- Grounded context construction
- Citation-aware generation

</td>
<td width="50%" valign="top">

### Evaluation & RAGOps

- Golden Dataset design
- MRR / Hit@K / Recall@K / NDCG@K
- Citation validity / sentence coverage
- Numeric faithfulness / abstention
- Regression and promotion gates
- Data / embedding / evidence lineage

</td>
</tr>
<tr>
<td width="50%" valign="top">

### Reliability & Failure Analysis

- Hosted model failure-domain diagnosis
- Retry for transient API failures
- Batch-level checkpoint / resume
- Duplicate-runner advisory lock
- Fault injection and rollback checks
- Evaluator false-negative analysis

</td>
<td width="50%" valign="top">

### Runtime & Infrastructure

- Python 3.12
- FastAPI / SQLAlchemy
- PostgreSQL / pgvector
- Docker Compose
- GitHub Actions
- Terraform validation
- NVIDIA NIM / Nemotron
- httpx persistent transport

</td>
</tr>
</table>

---

## A result I care about

In the 167-page generation test, the LLM-as-judge scored correctness / groundedness / relevance at **1.000**, but a deterministic numeric evaluator still caught two unsupported numeric claims in one answer.

That is the kind of problem I want to solve: **not just making an LLM answer, but building the evaluation and operating structure that can detect when a seemingly good answer is still wrong.**

---

## Current Interests

**RAG / RAGOps · Finance AI · Policy Finance · Credit / Risk Decision Support · Valuation · AI Evaluation · Reliable AI Workflows**


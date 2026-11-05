<!--
  GitHub Profile README
  Theme: Quiet Systems | Dark engineering | Ice blue + silver
-->

<div align="center">
  <img src="https://raw.githubusercontent.com/ayumu-ml/ayumu-ml/main/profile_banner.png" alt="AI processing pipeline in ice blue and silver" width="100%">
</div>

---

<div align="center">

# AYUSH SHARMA

### AI APPLICATION ENGINEER · FULL-STACK AI ENGINEER

*Building useful software. Investigating complex system behavior. Making systems dependable.*

[![GitHub](https://img.shields.io/badge/GitHub-ayumu--ml-181717?style=for-the-badge&logo=github)](https://github.com/ayumu-ml)
[![Projects](https://img.shields.io/badge/PROJECTS-EXPLORE-2563EB?style=for-the-badge&logo=stackblitz&logoColor=white)](https://github.com/ayumu-ml?tab=repositories)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-CONNECT-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ayush-sharma-swe/)
[![Email](https://img.shields.io/badge/Email-ayush.sharma.swe%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ayush.sharma.swe@gmail.com)

</div>

```text
ayush@engineering:~$ whoami

AI Application Engineer | Full-Stack AI Engineer
I build and ship software systems that solve practical problems,
with a focus on AI applications, backend architecture, retrieval systems,
and security-aware engineering.

ayush@engineering:~$ current_focus
> Omnitome (v1.1.0)
> Local-first desktop AI document intelligence & neural sidecar
> Collaborative platform engineering & full-stack deployments

ayush@engineering:~$ availability
> Remote International | ~30 hrs/week | Part-time / Contract preferred
```

---

## `01` / ENGINEERING STACK

<div align="center">

**LANGUAGES**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/SQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)

**BACKEND & APIS**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js_22_LTS-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=black)

**FRONTEND & DELIVERY**

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Tauri](https://img.shields.io/badge/Tauri_v2.0-24C8DB?style=flat-square&logo=tauri&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**AI & INFORMATION RETRIEVAL**

![PyTorch](https://img.shields.io/badge/PyTorch_CUDA_FP16-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![BGE-M3](https://img.shields.io/badge/BGE--M3_1024d-7C3AED?style=flat-square)
![BGE Reranker](https://img.shields.io/badge/BGE_Reranker_v2--m3-6D28D9?style=flat-square)
![Kokoro TTS](https://img.shields.io/badge/Kokoro--82M_TTS-EC4899?style=flat-square)
![PaddleOCR](https://img.shields.io/badge/PaddleOCR-14B8A6?style=flat-square)
![RAG](https://img.shields.io/badge/RAG_&_Retrieval-475569?style=flat-square)

</div>

---

## `02` / SELECTED SYSTEMS

### ◈ Omnitome (Flagship System)

**Local-first desktop AI document intelligence & reading platform**

[![Repository](https://img.shields.io/badge/REPOSITORY-Omnitome-181717?style=flat-square&logo=github)](https://github.com/ayumu-ml/Omnitome)
[![Release](https://img.shields.io/badge/RELEASE-v1.1.0-2563EB?style=flat-square)](https://github.com/ayumu-ml/Omnitome/releases/tag/v1.1.0)
![Status](https://img.shields.io/badge/STATUS-SHIPPED_&_MAINTAINED-16A34A?style=flat-square)

A local-first desktop application designed to turn dense technical documents, textbooks, and research papers into structured, interactive knowledge workspaces while keeping private files completely on-device.

- Multiformat document ingestion (PDF, EPUB, TXT, DOCX) and structured chapter hierarchy extraction.
- Local neural pipeline: PyTorch FP16 CUDA sidecar running BGE-M3 (1024d dense embeddings), BGE Reranker v2-m3, Kokoro-82M TTS, and PaddleOCR with CPU fallbacks.
- Explicit model lifecycle manager (`sidecars/python/lifecycle.py`) with lazy loading, in-flight request protection, configurable TTL idle eviction, and dynamic warming. Node.js orchestrator remains the sole SQLite writer.
- Repository-reported benchmarks: 296 MB peak Node.js RSS during ingestion, 174 MiB idle GPU allocation after eviction (~3.2 GB VRAM reclaimed), 16-chunk embedding batch reduced from ~124s to <1s, alongside historical stress benchmarks of ~6.3 GB RAM / ~4.3 GB VRAM.
- Desktop packaging via Tauri v2.0 (Rust) + Node.js 22 LTS orchestrator + 1.95 GB Windows desktop release installer with 61 unit/regression suites (including 13/13 passing lifecycle tests), 17 Rust supervisor tests, 10/10 corpus gate fixtures, and 90 procedural sound stems.

**Architecture**: `Tauri v2.0 (Rust)` → `Node.js 22 LTS orchestrator (Sole SQLite Writer)` → `SQLite WAL` → `FastAPI neural sidecar (CUDA FP16)`

---

### ◈ Cape Neto CRM

**Full-stack sales & pipeline management platform**

[![Live App](https://img.shields.io/badge/LIVE_APPLICATION-Visit-16A34A?style=flat-square&logo=vercel&logoColor=white)](https://cape-neto-crm.vercel.app/)
[![Source](https://img.shields.io/badge/SOURCE_CODE-GitHub-181717?style=flat-square&logo=github)](https://github.com/ayumu-ml/cape-neto-crm)
[![API Docs](https://img.shields.io/badge/API_DOCS-Open-2563EB?style=flat-square&logo=fastapi&logoColor=white)](https://cape-neto-crm-backend.onrender.com/docs)

A production CRM covering leads, clients, deals, tasks, sales activities, and real-time pipeline analytics.

- React 18 frontend deployed on Vercel with responsive deal pipeline stages and activity logs.
- FastAPI REST backend deployed on Render with JWT authentication and 3-tier role-based access control (Admin, Sales representative, Viewer).
- Dual database portability: SQLite deployed on Render and local development (`render_as_batch=True` with 3 versioned migrations) with SQLAlchemy 2.0 dialect adaptation for PostgreSQL.
- Comprehensive endpoint test suite (14 documented passing pytest regression tests) verifying schema constraints and auth boundaries.

**Architecture**: `React 18 / Vite` → `FastAPI REST` → `SQLAlchemy 2.0` → `SQLite (Render Deployed / Local) with PostgreSQL dialect compatibility`

---

### ◈ PlanRight

**Collaborative curriculum intelligence & RAG platform**

[![Case Study](https://img.shields.io/badge/CASE_STUDY-Open-2563EB?style=flat-square&logo=vercel&logoColor=white)](https://planright-case-study.vercel.app/)
![Role](https://img.shields.io/badge/ROLE-Infrastructure_&_Security_Engineer-7C3AED?style=flat-square)
![Status](https://img.shields.io/badge/STATUS-COLLABORATIVE_PRODUCTION-16A34A?style=flat-square)

A specialized curriculum intelligence platform designed for South African CAPS educational standards, enabling teachers and administrators to query lesson frameworks and syllabus constraints with verified citations (inspection grounded in Career Evidence Map).

- Dual-level chunking architecture combining CAPS curriculum metadata with dense semantic embeddings via Supabase pgvector.
- High-efficiency Edge Functions for low-latency retrieval and context assembly.
- Rigorous security boundaries: cryptographic JWT verification via `supabaseClient.auth.getUser`, 59 rewritten/remediated RLS policies addressing 73 database warnings.
- Collaborative professional repository with a 257-commit git history scrubbed via git-filter-repo for committed secret cleanup (not sole platform ownership).

**Architecture**: `React / TypeScript` → `Supabase Edge Functions` → `PostgreSQL + pgvector` → `Curriculum RAG`

---

### ◈ ChromeMind

**Privacy-conscious browser AI assistant**

[![Repository](https://img.shields.io/badge/REPOSITORY-ChromeMind-181717?style=flat-square&logo=github)](https://github.com/ayumu-ml/ChromeMind)
![Status](https://img.shields.io/badge/STATUS-ARCHIVED_REFERENCE_BUILD_v1.2.0-64748B?style=flat-square)
![Manifest V3](https://img.shields.io/badge/CHROME_EXTENSION-MV3-4285F4?style=flat-square&logo=googlechrome&logoColor=white)

An archived reference build of a Chrome Manifest V3 extension exploring on-device AI integration and privacy boundaries.

- Manifest V3 compliant service-worker architecture and side-panel interface.
- Three explicit privacy modes: Chrome on-device only (cloud never contacted), Chrome on-device first with configurable cloud fallback (Gemini/OpenRouter/HuggingFace with user keys), or Cloud only.
- Strict client-side data boundaries preventing page content leakage without explicit user action, verified by 28 documented unit tests.

---

## `03` / PROFESSIONAL EXPERIENCE

### ◈ Cape Neto Solutions
**Software & AI Projects Intern** · *Feb 2026 – Apr 2026* (Remote)
- Built the foundational full-stack prototype of the internal sales CRM (React frontend, FastAPI backend, SQLite persistence).
- Investigated automated lead scoring algorithms and AI-assisted qualification workflows.
- Implemented core JWT authentication and secure database modeling practices.
- *Note: Subsequent production CRM features, hosted deployments, and client engagements represent distinct operational work.*

---

## `04` / ACADEMIC CREDENTIALS

- 🎓 **BSc in Computer Science** — University of the People
  - **Status**: 120/120 credits completed | GPA: 3.76/4.00 | *Degree conferral pending university processing*
  - **Capstone/Final Course**: CS 4407 — Data Mining and Machine Learning (**Grade: 100/100**, LMS calculated 99.7%)
- 🛡️ **Undergraduate Certificate in Network and Application Security** — Awarded April 2024
  - Focused on secure software lifecycle, defensive architecture, access control, and network security protocols.

---

## `05` / ENGINEERING PRINCIPLES

```python
engineering_principles = {
    "architecture": "Understand the system before changing it",
    "reliability":  "Make failures observable and recoverable",
    "performance":  "Measure resource costs; optimize bottlenecks",
    "security":     "Respect identity, access, and data boundaries",
    "delivery":     "Validate behavior, not just successful builds",
}
```

> **AI-Assisted Engineering Philosophy**:  
> I use AI-assisted development as an engineering tool, not a substitute for engineering judgment. I define problems, reason through architectural trade-offs, direct implementation, and rigorously review, test, and validate the resulting systems.

---

## `06` / AVAILABILITY & CONNECT

I am currently open to **remote international opportunities**, with a strong preference for **part-time or contract engagements (~30 hours/week)**.

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-ayumu--ml-181717?style=for-the-badge&logo=github)](https://github.com/ayumu-ml)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-CONNECT-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ayush-sharma-swe/)
[![Email](https://img.shields.io/badge/Email-ayush.sharma.swe%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:ayush.sharma.swe@gmail.com)

**Explore the repositories. Inspect the implementation. Verify the tests.**

</div>
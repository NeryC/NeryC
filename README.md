# Hi there, I'm Nery Cano! 👋
[![GDG Asunción](https://img.shields.io/badge/Google_Developer_Group-Organizer-blue?style=for-the-badge&logo=google&logoColor=white)](https://gdg.community.dev/gdg-asuncion/)
[![Portfolio](https://img.shields.io/badge/Portfolio-neryc.github.io-1F4E79?style=for-the-badge&logo=githubpages&logoColor=white)](https://neryc.github.io/nery-cano-portfolio/)
[![CV](https://img.shields.io/badge/Download_CV-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1_5A8e-xGep_Wd1lRP6r0sFIMgUQvmkQ9/view?usp=sharing)

## Senior Full-Stack Engineer · AI/LLM Systems · Next.js · Anthropic Claude · Open to Remote

I am a seasoned developer with **7+ years of experience** crafting modern web applications, now specializing in **AI/LLM-integrated systems built end-to-end**. Expert in **Next.js**, **React**, **Node.js**, **Python**, and **PostgreSQL/Supabase pgvector**, with deep experience designing **multi-agent orchestrations** on **Anthropic Claude** and the **Vercel AI SDK v6**. Strong on inclusive design (WCAG), web performance, and SEO. A runner at heart — I bring the same endurance to debugging and shipping.

- 🤖 **Recent impact:** cut clinician documentation time **60%** at a US healthcare platform with Anthropic Claude + multi-agent orchestration on Next.js 15.
- 🛠️ **Currently shipping:** three public AI agents (RAG with memory, multi-agent code reviewer, autonomous research agent) — see below.
- ♿ **Accessibility:** WCAG 2.1 across enterprise and clinician interfaces.
- 🏃🏻‍♂️ **Fun fact:** marathon runner. Same logic for long-haul backend problems.

---

### 🤖 Featured AI / LLM Projects (2026)

> Built end-to-end on my own time. All three are deployed and have detailed READMEs.

#### 🧠 [RAG Agent with Memory](https://github.com/NeryC/rag-agent-memory) · [live demo ↗](https://rag-agent-memory.vercel.app)
Upload PDFs, chat with them, get cited answers. The agent searches the web when documents don't cover a topic and **remembers facts about you across sessions**.

- **Zero-dependency PDF parser** (Node `zlib` + regex) to dodge `pdfjs-dist`'s `DOMMatrix is not defined` on Vercel serverless.
- **Dual memory:** top-5 chunks + top-3 user memories per query; long-term facts extracted asynchronously by Claude Haiku 4.5 and re-vectorized.
- Voyage AI `input_type` document/query split — lifted relevant-pair similarity from ~0.25 noise floor to 0.5–0.8.
- *Stack:* Next.js 16 · AI SDK v6 · Claude Sonnet 4.6 + Haiku 4.5 · Voyage AI `voyage-3` · Supabase pgvector (HNSW) · Vercel Blob · Exa AI.

#### 🔍 [Multi-Agent Code Reviewer](https://github.com/NeryC/multi-agent-code-reviewer) · [live demo ↗](https://multi-agent-code-reviewer-sable.vercel.app)
Three specialist agents (security, performance, maintainability) review code in parallel; a supervisor consolidates a 0–100 scored report.

- `Promise.all` parallel agents → ~15s total instead of ~45s sequential.
- **Zod schemas as agent contracts** with `generateObject` → zero parsing, fully typed findings.
- Single SSE endpoint → no Redis/KV needed for job state.
- *Stack:* Next.js 16 · AI SDK v6 · Claude Sonnet 4.6 (specialists) + Haiku 4.5 (supervisor) · Vercel AI Gateway · Zod v4 · native SSE.

#### 🌐 [Research Agent](https://github.com/NeryC/research-agent) · [live demo ↗](https://research-agent-three-pi.vercel.app)
Autonomous research assistant that searches the web, reads pages, and synthesizes a cited Markdown answer.

- `ToolLoopAgent` + `stepCountIs(8)` — declarative agent loop, no hand-rolled `while` over `streamText`.
- **Terminal tool with no `execute`** (`finalAnswer`) — clean stop signal with a fully typed payload.
- Vercel AI Gateway = single key + automatic provider failover.
- *Stack:* Next.js 16 · AI SDK v6 ToolLoopAgent · Claude Sonnet 4.6 · Vercel AI Gateway · Exa AI · Tailwind v4 + shadcn/ui · Vitest.

---

### 🛠️ Tech Stack

| Frontend | Backend & Data | AI / LLM | DevOps & Tools |
| :--- | :--- | :--- | :--- |
| ![React](https://img.shields.io/badge/-React-45b8d8?style=flat-square&logo=react&logoColor=white) ![Next.js](https://img.shields.io/badge/-Next.js-000000?style=flat-square&logo=next.js&logoColor=white) ![TypeScript](https://img.shields.io/badge/-TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white) | ![Node.js](https://img.shields.io/badge/-Node.js-43853d?style=flat-square&logo=node.js&logoColor=white) ![Python](https://img.shields.io/badge/-Python-3776ab?style=flat-square&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) | ![Anthropic](https://img.shields.io/badge/-Anthropic_Claude-D4A27F?style=flat-square&logo=anthropic&logoColor=white) ![Vercel AI SDK](https://img.shields.io/badge/-Vercel_AI_SDK_v6-000000?style=flat-square&logo=vercel&logoColor=white) | ![AWS](https://img.shields.io/badge/-AWS-232f3e?style=flat-square&logo=amazon-aws&logoColor=white) ![GCP](https://img.shields.io/badge/-GCP-4285F4?style=flat-square&logo=google-cloud&logoColor=white) |
| ![React Native](https://img.shields.io/badge/-React_Native-45b8d8?style=flat-square&logo=react&logoColor=white) ![Expo](https://img.shields.io/badge/-Expo-000020?style=flat-square&logo=expo&logoColor=white) ![Tailwind](https://img.shields.io/badge/-Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) | ![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white) ![Supabase](https://img.shields.io/badge/-Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white) ![Prisma](https://img.shields.io/badge/-Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white) | ![pgvector](https://img.shields.io/badge/-pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![RAG](https://img.shields.io/badge/-RAG_pipelines-7C3AED?style=flat-square) ![Multi--agent](https://img.shields.io/badge/-Multi--agent-2EA44F?style=flat-square) | ![Docker](https://img.shields.io/badge/-Docker-2496ed?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/-GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white) |
| ![Vue](https://img.shields.io/badge/-Vue.js-4FC08D?style=flat-square&logo=vue.js&logoColor=white) ![GraphQL](https://img.shields.io/badge/-GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white) ![Zustand](https://img.shields.io/badge/-Zustand-443E38?style=flat-square) | ![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white) ![Redis](https://img.shields.io/badge/-Redis-DC382D?style=flat-square&logo=redis&logoColor=white) | ![OCR](https://img.shields.io/badge/-AWS_Comprehend_Medical-FF9900?style=flat-square&logo=amazon-aws&logoColor=white) ![Voyage](https://img.shields.io/badge/-Voyage_AI-000000?style=flat-square) ![Exa](https://img.shields.io/badge/-Exa_AI-1E90FF?style=flat-square) | ![Vercel](https://img.shields.io/badge/-Vercel-000000?style=flat-square&logo=vercel&logoColor=white) ![Sentry](https://img.shields.io/badge/-Sentry-362D59?style=flat-square&logo=sentry&logoColor=white) |
| ![MobX](https://img.shields.io/badge/-MobX-FF9955?style=flat-square&logo=mobx&logoColor=white) ![Salesforce](https://img.shields.io/badge/-Salesforce_Apex-00A1E0?style=flat-square&logo=salesforce&logoColor=white) | ![SQLAlchemy](https://img.shields.io/badge/-SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white) ![Contentful](https://img.shields.io/badge/-Contentful-2478CC?style=flat-square&logo=contentful&logoColor=white) | ![Cursor](https://img.shields.io/badge/-Cursor-000000?style=flat-square) ![Claude Code](https://img.shields.io/badge/-Claude_Code-D4A27F?style=flat-square) ![Gemini CLI](https://img.shields.io/badge/-Gemini_CLI-4285F4?style=flat-square&logo=google&logoColor=white) | ![Firebase](https://img.shields.io/badge/-Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black) ![Electron](https://img.shields.io/badge/-Electron-47848F?style=flat-square&logo=electron&logoColor=white) |

---

### 💼 Professional Highlights

Most of my paid work lives in **private enterprise repositories**. Here's a summary:

* **Healthcare Platform – Jobsity · Senior Full-Stack Developer (Feb 2025 – Present):** Architected and shipped Ebervetter, a clinician-facing AI-integrated platform on Next.js 15 + Supabase + Anthropic Claude.
  * *Tech:* Next.js 15, React Native, GraphQL, React Query, AWS Transcribe/Comprehend Medical, Anthropic Claude, OCR.
  * *Impact:* **60% reduction** in clinician documentation time via multi-agent orchestration and voice-to-text medical entity extraction.
* **Education Platform – Penguin Academy · Lead Developer, CodePro (Feb 2024 – Jan 2025):** Sole developer of the CodePro bootcamp platform (independent contractor).
  * *Tech:* Next.js, AWS S3, PostgreSQL, Firebase, Cloudflare, Vercel, Heroku.
  * *Impact:* Enhanced engagement for **90+ students** with **99.9% uptime**.
* **Retail E-Commerce – Jobsity · Full-Stack Developer (Jan 2023 – Jan 2024):** Performance and UX work on high-traffic storefronts for Hollister & Abercrombie & Fitch.
  * *Tech:* Next.js (SSR/SSG), React, Node.js, Contentful, Docker, RTL, Tailwind CSS.
* **Enterprise Maintenance – Kenility · Full-Stack Developer (Apr 2022 – Jan 2023):** Maintained core features of the **ZenBusiness** platform.
* **Crypto Fintech – Chiatk · Front-end Developer (Jan 2021 – Apr 2023, side project):** Real-time landing pages for a cryptocurrency fintech (React, Vue, Electron).
* **Salesforce Ecosystem – Oktana · Full-Stack Engineer (Nov 2018 – Mar 2022):** Enterprise web, mobile and desktop solutions for international clients (Apex, React, React Native, Electron).

---

### 🧪 Other Personal Projects

* **AdminRent — Multi-tenant SaaS for residential property management** *(in progress)*
  * *Polyglot architecture:* Next.js admin dashboard, Flask REST API, Flutter mobile app, and a TypeScript microservice integrating Paraguay's SIFEN e-invoicing (SOAP, XML signing).
  * *Web:* **Next.js (App Router, Server Components), TypeScript, Tailwind, TanStack Query, Supabase SSR, Axios.**
  * *API:* **Python · Flask, SQLAlchemy + Alembic, PostgreSQL, PyJWT, Resend, WeasyPrint, OpenPyXL, Gunicorn.**
  * *Mobile:* **Flutter, Riverpod, Dio, Firebase Auth + FCM, sqflite.**
  * *SIFEN microservice:* **Node.js + TypeScript, Express, PostgreSQL, SOAP, xml-crypto + node-forge, Zod, node-cron, Docker.**
  * *DevOps:* Docker, Railway, automated migrations on deploy.

---

### 🌟 Community & Leadership

* **Organizer @ [GDG Asunción](https://gdg.community.dev/gdg-asuncion/)** — leading the local Google Developer Group: events, workshops, and tech talks for the Paraguayan ecosystem.
* **Tech Evangelist** — sharing notes on web performance, AI/LLM systems, and career growth.

---

### 🎓 Education

* **B.S. in Computer Engineering** — Universidad Autónoma de Asunción *(Expected Graduation: 2026 — Thesis Phase)*

---

### 📊 GitHub Stats

<p align="center">
  <img src="https://github.com/NeryC/NeryC/blob/output/github-contribution-grid-snake-dark.svg" alt="Snake animation" />
</p>

### 🚀 Career Snapshot

<div align="center">
  <img src="https://img.shields.io/badge/Experience-7%2B_Years-blue?style=for-the-badge&logo=awesomelists&logoColor=white" />
  <img src="https://img.shields.io/badge/Focus-AI%2FLLM_Systems_%26_HealthTech-2ea44f?style=for-the-badge&logo=anthropic&logoColor=white" />
  <img src="https://img.shields.io/badge/Stack-Next.js_%2B_Anthropic_Claude-000000?style=for-the-badge&logo=vercel&logoColor=white" />
  <img src="https://img.shields.io/badge/Community-GDG_Organizer-4285F4?style=for-the-badge&logo=google&logoColor=white" />
</div>

---

### 📈 Coding Habits
<p align="center">
  <img src="./profile-summary-card-output/tokyonight/0-profile-details.svg" alt="Profile Details" />
</p>

<p align="center">
  <img src="./profile-summary-card-output/tokyonight/3-stats.svg" alt="Top Languages" width="48%" />
  <img src="./profile-summary-card-output/tokyonight/1-repos-per-language.svg" alt="Productive Time" width="48%" />
</p>

# SD4ALL AI Lab — Tool Landscape & Architecture Decisions
_Updated: 20 Mar 2026_

## Core Architecture Decision

**Claude Code agents are the primary automation engine.** Not n8n, not custom ML pipelines — Claude Code + Agent SDK can reason, call APIs, read/write data, and orchestrate complex multi-step business processes out of the box.

This means:
- No need to learn complex workflow tools (n8n was evaluated and dropped — too complex for the value)
- AI agents are built as Claude Code agents that connect to GoHighLevel and PushPress via API
- Learning happens through building real business automations, not abstract exercises

---

## Tool Stack

### Adopted

| Tool | Category | Why We Chose It |
|------|----------|-----------------|
| **Claude Code + Agent SDK** | Agent framework (core) | Most capable reasoning. Can call APIs, orchestrate flows, handle complex business logic. This is where our 5 agents live. |
| **Codex (OpenAI)** | Agent framework (alt) | Evaluate alongside Claude for specific tasks. Good to have options. |
| **Gumloop** | Visual/media workflows | Already has a working video analysis workflow (visual coach). Best-in-class for media processing pipelines. Not replaceable by code agents. |
| **Claude (Anthropic API)** | LLM (primary) | Best reasoning for business process agents. Powers AGT-01 through AGT-05. |
| **Gemini 2.5 Flash** | LLM (cost-effective) | 20-30% cheaper tokens. Use for high-volume, simpler tasks where Claude's reasoning isn't needed. |
| **GoHighLevel** | CRM & marketing automation | Already in use. Connect via API for lead management, email/SMS, pipelines. |
| **PushPress** | Student management | Already in use. Connect via API for attendance, memberships, scheduling. |
| **Python + pandas** | Data analysis | Industry standard. Notebooks for exploration, scripts for pipelines. |
| **Streamlit** | Dashboards | Fastest path from Python script to web dashboard. Free, open source. |
| **Obsidian** | Knowledge base | Captain's Logs, learning journal, process notes. Local-first, markdown. |

### Evaluated & Dropped

| Tool | Why Dropped |
|------|-------------|
| **n8n** | Too complex for what Claude Code agents can do natively. Adds unnecessary infrastructure. |
| **Abstract ML exercises** | Logistic regression from scratch doesn't help run a martial arts business. ML concepts learned through real data (Phase 2-3). |
| **Dify AI** | Interesting but redundant with Claude Code agents. Keep as fallback. |

### Tracked for Later

| Tool | When | Why |
|------|------|-----|
| **OpenClaw** | Phase 3 (Aug-Dec 2026) | 247K GitHub stars. Evaluate for WhatsApp/Telegram student-facing bot. Self-hosted, multi-channel. Security concerns noted — needs guardrails for student data. |
| **MindsDB** | Phase 2 (Jun-Aug 2026) | Natural language queries over data lake. Would let instructors ask "how many students attended sparring this month?" |
| **NVIDIA Cosmos/Isaac** | 2027+ | Physical AI / robotics. Not relevant for martial arts operations now. Track for future facility automation. |

---

## Agent Architecture

```
                    ┌─────────────────────┐
                    │   Claude Code        │
                    │   Agent SDK          │
                    └──────┬──────────────┘
                           │
         ┌─────────┬───────┼───────┬──────────┐
         │         │       │       │          │
      AGT-01    AGT-02  AGT-03  AGT-04    AGT-05
      Lead      Retain  Class   Finance   Marketing
      Follow-up Alert   Sched   Reporter  Analyst
         │         │       │       │          │
         └────┬────┘       │      └────┬──────┘
              │            │           │
         GoHighLevel   PushPress   Data Lake
         (CRM API)    (Student    (CSV/SQL)
                       Mgmt API)
```

**Gumloop** operates independently for video/media workflows:
```
Class footage → Gumloop → Visual Coach Report → Instructor feedback
```

**OpenClaw** (Phase 3) would add a student-facing layer:
```
Student WhatsApp msg → OpenClaw → Claude API → Response
                                    ↓
                              GoHighLevel (book trial, FAQ)
```

---

## API Integration Map

| System | API Available? | Key Endpoints | Priority |
|--------|---------------|---------------|----------|
| GoHighLevel | Yes (REST API) | Contacts, Opportunities, Conversations, Calendars | Phase 0-1 |
| PushPress | Yes (REST API) | Members, Check-ins, Classes, Plans | Phase 0-1 |
| Claude API | Yes | Messages, Tools | Phase 1 |
| Gemini API | Yes | GenerateContent | Phase 2 |

---

## Decision Log

| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-03-20 | Claude Code agents as core framework | Most capable, least infrastructure overhead |
| 2026-03-20 | Drop n8n | Too complex; agents handle orchestration natively |
| 2026-03-20 | Keep Gumloop for video | Already working; video analysis is its strength |
| 2026-03-20 | Replace abstract ML with applied learning | Business impact > academic completeness |
| 2026-03-20 | Defer OpenClaw to Phase 3 | Evaluate after core agents are running |

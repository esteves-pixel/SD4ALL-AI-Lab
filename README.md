# SD4ALL-AI-Lab · Roadmap v2.0
_Updated: 20 Mar 2026_

> **"Good people becoming more capable together."**

An AI-powered Business Process Management system for Self Defense 4 All — built by doing, not by theory.

---

## Architecture

```
Claude Code Agents ──► GoHighLevel (CRM) + PushPress (Students)
        │
        ├── AGT-01  Lead Follow-up
        ├── AGT-02  Retention Alerts
        ├── AGT-03  Class Scheduler
        ├── AGT-04  Finance Reporter
        └── AGT-05  Marketing Analyst

Gumloop ──► Video Analysis (Visual Coach)
OpenClaw ──► WhatsApp/Telegram Student Bot (Phase 3)

Data: GoHighLevel + PushPress → Python/pandas → KPI Dashboards
BPM:  SIPOC methodology across 7 macro processes
```

---

## Phase 0 · Foundation Reset (Mar — Apr 2026)
_Strategic clarity + dev environment + tool architecture_

**Processes:** Layer 0 (Strategic), MP-07 (Tech & Data)

| Task | Status |
|------|--------|
| Install Python 3.12, Conda, Git, VS Code | ✅ |
| Create repo + project structure + BPM framework | ✅ |
| Mac development environment setup guide | ✅ |
| Master context & brand voice document (v6) | ✅ |
| Fill Layer 0: Mission, Vision, 3 OKRs | ✅ |
| Define agent architecture & tool stack | ✅ |
| Map GoHighLevel + PushPress APIs | ⬜ |
| Document architecture in `docs/TOOLS_LANDSCAPE.md` | ✅ |

**Learn by doing:** API exploration, JSON, environment variables, Git workflow

---

## Phase 1 · Quick Wins — Lead & Retention (Apr — Jun 2026)
_Solve the two biggest revenue leaks with Claude Code agents_

**Processes:** MP-01 (Student Lifecycle), MP-04 (Growth & Marketing)

| Task | Status |
|------|--------|
| Document MP-01 SIPOC sub-processes (lead → trial → enroll → retain) | ⬜ |
| **AGT-01:** Lead Follow-up Agent — monitor leads, draft follow-ups, book trials | ⬜ |
| **AGT-02:** Retention Alert Agent — flag at-risk students from attendance data | ⬜ |
| Consultation reminder automation (GoHighLevel API) | ⬜ |
| Enhance Gumloop visual coach — expand to instructor feedback analysis | ⬜ |
| Document MP-04 SIPOC (Growth & Marketing) | ⬜ |

**KPIs:** Lead→Trial conversion, consultation show-up rate, 6-week retention

**Learn by doing:** Claude API, prompt engineering, agent architecture, webhook/API integration

---

## Phase 2 · Data & Intelligence (Jun — Aug 2026)
_Turn scattered data into decisions_

**Processes:** MP-07 (Tech & Data), MP-02 (Class Delivery), MP-05 (Finance)

| Task | Status |
|------|--------|
| Build data pipeline: GoHighLevel + PushPress → structured data | ⬜ |
| Document MP-02 (Class Delivery) SIPOC | ⬜ |
| Document MP-05 (Finance & Admin) SIPOC | ⬜ |
| **AGT-04:** Finance Reporter — weekly/monthly revenue reports & trends | ⬜ |
| Build KPI dashboard (Streamlit or notebook) | ⬜ |
| `hello_data.ipynb` — real SD4ALL data analysis | ⬜ |

**KPIs:** Revenue trend, class utilization, cost per lead

**Learn by doing:** Data modeling, SQL/pandas, visualization, ETL concepts

---

## Phase 3 · Scale & Optimize (Aug — Dec 2026)
_Full BPM system, ML on real data, reduce founder load_

**Processes:** MP-03, MP-06, all remaining SIPOC docs

| Task | Status |
|------|--------|
| Complete all 7 macro process SIPOC documentation | ⬜ |
| **AGT-03:** Class Scheduler — optimize instructor allocation | ⬜ |
| **AGT-05:** Marketing Analyst — content suggestions, campaign analysis | ⬜ |
| Document MP-06 (People & Culture) — Trainer of Trainers program | ⬜ |
| Churn prediction model on real student data | ⬜ |
| Revenue forecasting notebook | ⬜ |
| Evaluate OpenClaw for WhatsApp/Telegram student bot | ⬜ |

**Business targets by Dec 2026:**
- 175–200 active students (from 65)
- $35K+ monthly revenue
- Founder teaching load <50% of classes
- 6-week retention >50%

**Learn by doing:** ML classification (churn), time series (revenue), agent orchestration at scale

---

## Tool Stack

| Category | Tool | Notes |
|----------|------|-------|
| Agent framework | **Claude Code + Agent SDK** | Core automation engine |
| Agent framework (alt) | **Codex (OpenAI)** | Evaluate for specific tasks |
| Visual/media workflows | **Gumloop** | Video analysis, visual coach (already built) |
| Multi-channel bot | **OpenClaw** | WhatsApp/Telegram (Phase 3) |
| LLM (primary) | **Claude** | Best reasoning for business agents |
| LLM (cost-effective) | **Gemini 2.5 Flash** | High-volume, simpler tasks |
| CRM | **GoHighLevel** | Existing — connect via API |
| Student management | **PushPress** | Existing — connect via API |
| Data & dashboards | **Python + pandas + Streamlit** | Analysis + visualization |
| Knowledge base | **Obsidian** | Captain's Logs, learning journal |

---

## Repository Structure

```
SD4ALL-AI-Lab/
├── CLAUDE.md              ← Project context for Claude
├── README.md              ← This roadmap
├── docs/                  ← Setup guides, tool landscape
├── bpm/                   ← Business Process Management (SIPOC)
│   ├── layer0-strategic/  ← Mission, vision, OKRs
│   ├── macro-processes/   ← MP-01 through MP-07
│   └── templates/         ← SIPOC template for new processes
├── agents/                ← AI agents and shared skills
├── data/                  ← Data lake (raw, processed, KPIs)
└── notebooks/             ← Jupyter notebooks for analysis
```

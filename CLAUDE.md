# SD4ALL AI Lab — Project Context

## What Is This Project?
An end-to-end **Business Process Management (BPM) system** for **Self Defense 4 All (SD4ALL)**, a martial arts / self-defense business. The system documents, executes, measures, and optimizes all business operations using the **SIPOC methodology**.

## Repository Structure
```
SD4ALL-AI-Lab/
├── CLAUDE.md              ← This file (project context for Claude)
├── README.md              ← Roadmap v2.0 (4 phases)
├── docs/                  ← Setup guides, tool landscape
│   ├── TOOLS_LANDSCAPE.md ← Tool choices & architecture decisions
│   └── MAC_SETUP_*.md     ← Dev environment guides
├── bpm/                   ← Business Process Management (SIPOC)
│   ├── layer0-strategic/  ← Mission, vision, OKRs (filled in)
│   ├── macro-processes/   ← MP-01 through MP-07
│   └── templates/         ← SIPOC template for new processes
├── agents/                ← AI agents (AGT-01 through AGT-05)
├── data/                  ← Data lake (raw, processed, KPIs)
└── notebooks/             ← Jupyter notebooks for analysis
```

## Tool Stack
- **Agent framework:** Claude Code + Agent SDK (core), Codex (evaluate)
- **Visual/media:** Gumloop (video analysis, visual coach)
- **Multi-channel bot:** OpenClaw (Phase 3, WhatsApp/Telegram)
- **LLMs:** Claude (primary reasoning), Gemini 2.5 Flash (cost-effective)
- **Existing systems:** GoHighLevel (CRM), PushPress (student mgmt)
- **Data:** Python + pandas + Streamlit dashboards
- **Knowledge:** Obsidian (Captain's Logs)

See `docs/TOOLS_LANDSCAPE.md` for full rationale and architecture diagrams.

## SIPOC Macro Processes
- **MP-01** Student Lifecycle (lead → enrolled → retained → alumni)
- **MP-02** Class Delivery (scheduling, instruction, grading)
- **MP-03** Business Ops (facilities, supplies, compliance)
- **MP-04** Growth & Marketing (campaigns, partnerships, events)
- **MP-05** Finance & Admin (billing, payroll, accounting)
- **MP-06** People & Culture (hiring, training, instructor development)
- **MP-07** Tech & Data (systems, AI agents, data platform)

## AI Agents
- **AGT-01** Lead Follow-up — monitors GoHighLevel, drafts follow-ups, books trials
- **AGT-02** Retention Alert — flags at-risk students from PushPress attendance data
- **AGT-03** Class Scheduler — optimizes instructor allocation
- **AGT-04** Finance Reporter — weekly/monthly revenue reports & trends
- **AGT-05** Marketing Analyst — content suggestions, campaign analysis

## Architecture Layers
- **Layer 0:** Strategic (mission, vision, OKRs, KPIs)
- **Layer 1:** Macro processes (7 main processes)
- **Layer 2:** Sub-processes (detailed SIPOC for each)
- **Layer 3:** Execution (Claude Code agents, Gumloop workflows, data capture)

## Key Principles
- Every process generates data → data lake → KPIs → decisions
- AI agents support execution, humans own the processes
- SIPOC template ensures consistency across all documentation
- Processes are interconnected (outputs of one feed inputs of another)
- Learn by building real business tools, not abstract exercises

## Owner
GitHub: esteves-pixel

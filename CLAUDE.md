# SD4ALL AI Lab — Project Context

## What Is This Project?
An end-to-end **Business Process Management (BPM) system** for **Self Defense 4 All (SD4ALL)**, a martial arts / self-defense business. The system documents, executes, measures, and optimizes all business operations using the **SIPOC methodology**.

## Repository Structure
```
SD4ALL-AI-Lab/
├── CLAUDE.md              ← This file (project context for Claude)
├── README.md              ← Roadmap
├── docs/                  ← Setup guides, how-tos
├── bpm/                   ← Business Process Management (SIPOC)
│   ├── layer0-strategic/  ← Mission, vision, OKRs
│   ├── macro-processes/   ← MP-01 through MP-07
│   └── templates/         ← SIPOC template for new processes
├── data/                  ← Data lake (raw, processed, KPIs)
├── agents/                ← AI agents and shared skills
└── notebooks/             ← Jupyter notebooks for analysis
```

## SIPOC Macro Processes
- **MP-01** Student Lifecycle (lead → enrolled → retained → alumni)
- **MP-02** Class Delivery (scheduling, instruction, grading)
- **MP-03** Business Ops (facilities, supplies, compliance)
- **MP-04** Growth & Marketing (campaigns, partnerships, events)
- **MP-05** Finance & Admin (billing, payroll, accounting)
- **MP-06** People & Culture (hiring, training, instructor development)
- **MP-07** Tech & Data (systems, AI agents, data platform)

## Architecture Layers
- **Layer 0:** Strategic (goals, KPIs)
- **Layer 1:** Macro processes (7 main processes)
- **Layer 2:** Sub-processes (detailed SIPOC for each)
- **Layer 3:** Execution (tasks, agents, automations, data capture)

## Key Principles
- Every process generates data → data lake → KPIs → decisions
- AI agents support execution, humans own the processes
- SIPOC template ensures consistency across all documentation
- Processes are interconnected (outputs of one feed inputs of another)

## Owner
GitHub: esteves-pixel

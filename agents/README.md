# SD4ALL AI Agents & Skills

## Architecture

```
┌─────────────────────────────────────────────┐
│              ORCHESTRATOR                    │
│  (Claude Code / Agent SDK)                  │
│                                             │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐    │
│  │ Agent 1 │  │ Agent 2 │  │ Agent 3 │    │
│  │ Lead    │  │Retention│  │ Finance │    │
│  │ Mgmt    │  │ Monitor │  │ Report  │    │
│  └────┬────┘  └────┬────┘  └────┬────┘    │
│       │            │            │          │
│  ┌────┴────────────┴────────────┴────┐     │
│  │           SKILLS LIBRARY          │     │
│  │  • send-email    • query-data     │     │
│  │  • send-sms      • generate-report│     │
│  │  • update-crm    • schedule-class │     │
│  │  • slack-notify   • analyze-kpi   │     │
│  └───────────────────────────────────┘     │
│                    │                        │
│              ┌─────┴─────┐                  │
│              │ DATA LAKE │                  │
│              └───────────┘                  │
└─────────────────────────────────────────────┘
```

## Agent Registry

| Agent ID | Name | Macro Process | Status |
|----------|------|---------------|--------|
| AGT-01 | Lead Follow-up | MP-01 | Planned |
| AGT-02 | Retention Alert | MP-01 | Planned |
| AGT-03 | Class Scheduler | MP-02 | Planned |
| AGT-04 | Finance Reporter | MP-05 | Planned |
| AGT-05 | Marketing Analyst | MP-04 | Planned |

## Skills Library

Skills are reusable capabilities shared across agents:

| Skill | Description | Used By |
|-------|-------------|---------|
| send-email | Send templated emails | AGT-01, AGT-02 |
| query-data | Read from data lake | All agents |
| generate-report | Create PDF/markdown reports | AGT-04, AGT-05 |
| update-crm | Write to student records | AGT-01, AGT-02 |
| slack-notify | Post to Slack channels | All agents |

## How to Build an Agent

Each agent lives in its own folder:

```
agents/
├── README.md                ← You are here
├── agt-01-lead-followup/
│   ├── agent.md             ← Agent definition (prompt, tools, triggers)
│   ├── skills/              ← Agent-specific skills
│   └── tests/               ← Test scenarios
├── shared-skills/           ← Reusable skills library
└── config/                  ← Agent configuration
```

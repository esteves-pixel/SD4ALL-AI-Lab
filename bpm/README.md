# SD4ALL Business Process Management (BPM)

## SIPOC Methodology

**SIPOC** = Suppliers → Inputs → Process → Outputs → Customers

Each macro process in SD4ALL is documented using this framework to ensure
clarity, traceability, and measurability.

---

## Macro Process Map (Layers)

```
┌─────────────────────────────────────────────────────────────────┐
│                    LAYER 0: STRATEGIC                           │
│  Mission · Vision · Strategic Goals · KPIs                     │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────┴────────────────────────────────────┐
│                    LAYER 1: MACRO PROCESSES                     │
│                                                                 │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────────┐   │
│  │ MP-01    │  │ MP-02    │  │ MP-03    │  │ MP-04        │   │
│  │ Student  │→ │ Class    │→ │ Business │→ │ Growth &     │   │
│  │ Lifecycle│  │ Delivery │  │ Ops      │  │ Marketing    │   │
│  └──────────┘  └──────────┘  └──────────┘  └──────────────┘   │
│                                                                 │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐                     │
│  │ MP-05    │  │ MP-06    │  │ MP-07    │                     │
│  │ Finance  │  │ People & │  │ Tech &   │                     │
│  │ & Admin  │  │ Culture  │  │ Data     │                     │
│  └──────────┘  └──────────┘  └──────────┘                     │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────┴────────────────────────────────────┐
│                    LAYER 2: SUB-PROCESSES                       │
│  Each macro process breaks down into 3-8 sub-processes         │
│  (documented in individual SIPOC files)                         │
└────────────────────────────┬────────────────────────────────────┘
                             │
┌────────────────────────────┴────────────────────────────────────┐
│                    LAYER 3: EXECUTION                           │
│  Tasks · Agents · Automations · Data Capture                   │
│  → feeds into Data Lake for KPIs                               │
└─────────────────────────────────────────────────────────────────┘
```

---

## Folder Structure

```
bpm/
├── README.md                    ← You are here
├── layer0-strategic/
│   └── strategic-goals.md       ← Vision, mission, OKRs
├── macro-processes/
│   ├── MP-01-student-lifecycle/ ← Lead → Enrolled → Retained → Alumni
│   ├── MP-02-class-delivery/    ← Scheduling, instruction, grading
│   ├── MP-03-business-ops/      ← Facilities, supplies, compliance
│   ├── MP-04-growth-marketing/  ← Marketing, partnerships, events
│   ├── MP-05-finance-admin/     ← Billing, payroll, accounting
│   ├── MP-06-people-culture/    ← Hiring, training, instructor dev
│   └── MP-07-tech-data/         ← Systems, AI agents, data platform
└── templates/
    └── sipoc-template.md        ← Blank template for new processes
```

## How Processes Connect to Data & AI

Each process generates **execution data** that flows into the data lake:

```
Process Execution → Data Lake → KPIs → Dashboards
                                  ↓
                            AI Agents & Skills
                       (automate, alert, optimize)
```

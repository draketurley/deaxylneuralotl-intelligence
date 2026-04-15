# Concord Architecture Diagram + Sequence Flow

## 1) Concord Reference Architecture (Mermaid)

```mermaid
flowchart TB
    A[Environment Signals\nData, Policies, Events] --> B[Context Synthesizer]
    B --> C[Intent & Task Router]
    C --> D[Reasoning Core]
    D --> E[Capability Orchestrator]
    E --> F[Tool/Action Layer]
    F --> G[Outcome Verifier]
    G --> H[Regenerative Loop Manager]
    H --> B

    I[Policy & Governance Engine] --> C
    I --> D
    I --> E
    I --> F
    I --> G

    J[Memory Substrate\nEpisodic/Semantic/Operational] --> D
    J --> E
    G --> J

    K[Human Operator Console] <--> I
    K <--> G
```

## 2) Concord Sequence Flow (Mermaid)

```mermaid
sequenceDiagram
    participant Env as Environment
    participant Ctx as Context Synthesizer
    participant Core as Reasoning Core
    participant Cap as Capability Orchestrator
    participant Tool as Tool/Action Layer
    participant Gov as Governance Engine
    participant Ops as Human Operator

    Env->>Ctx: Emit signals/events
    Ctx->>Gov: Validate context confidence
    Gov-->>Ctx: Context policy decision
    Ctx->>Core: Provide grounded context package

    Core->>Gov: Request decision authorization
    Gov-->>Core: Constraints + allowed actions

    Core->>Cap: Generate plan and action intent
    Cap->>Gov: Check capability/control concord
    Gov-->>Cap: Approved/Denied/Escalate

    alt Approved
        Cap->>Tool: Execute bounded action
        Tool-->>Core: Return result/state
        Core->>Gov: Submit outcome + rationale
        Gov-->>Core: Accept + log
    else Escalate
        Gov->>Ops: Request human decision
        Ops-->>Gov: Approve/Reject/Modify
        Gov-->>Cap: Updated directive
    end

    Core->>Ctx: Trigger regenerative update if degraded
    Ctx-->>Core: Refined context and recovery state
```

## 3) Concord Control Checkpoints

1. **Cognitive checkpoint**: objective-policy consistency.
2. **Context checkpoint**: data quality and relevance confidence.
3. **Capability checkpoint**: tool readiness and action boundaries.
4. **Control checkpoint**: compliance, authority, and escalation trace.

## 4) Minimum Logging Requirements

- Decision intent hash
- Constraint set applied
- Action executed/blocked
- Outcome verification result
- Escalation path and final authority
- Recovery operations performed

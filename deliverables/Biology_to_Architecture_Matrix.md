# Biology-to-Architecture Matrix

| Axolotl Biological Trait | DNAI Engineering Principle | Architecture Pattern | Runtime Behavior | KPI Examples |
|---|---|---|---|---|
| Limb regeneration | Functional restoration after failure | Regenerative control loop + checkpoint replay | Auto-rebuild failed task chains and resume statefully | MTTR, recovery success rate |
| Tissue plasticity | Safe adaptive reconfiguration | Modular capability adapters with policy constraints | Adjusts strategy as context shifts without violating controls | Adaptation latency, error delta post-shift |
| Context-dependent regeneration | Environment-native adaptation | Context synthesizer + signal confidence weighting | Behavior changes based on verified context quality | Context-grounded accuracy, false-action rate |
| Scarless healing | High-quality recovery without long-term degradation | Rollback/roll-forward orchestration + quality guardrails | Returns to nominal performance after incidents | Post-incident quality variance |
| Developmental persistence (neoteny) | Continuous learning with retained oversight | Human-in-the-loop memory curation and policy gating | Learns incrementally while preserving core governance profile | Learning gain vs policy exceptions |
| Bioenergetic regulation | Resource-aware intelligence behavior | Dynamic budget manager (compute/tool/time ceilings) | Scales effort based on risk and business criticality | Cost per successful outcome, SLA adherence |

## Implementation Notes
- Each row should map to at least one observable metric in the production dashboard.
- No architecture element should be approved without both a resilience metric and a governance metric.
- Regenerative actions must remain auditable and reversible.

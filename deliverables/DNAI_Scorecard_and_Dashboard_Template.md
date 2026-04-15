# DNAI Scorecard + Dashboard Template

## A. DNAI Executive Scorecard (Monthly)

| Dimension | Metric | Formula/Definition | Target | Current | Trend | Owner | Status |
|---|---|---|---|---|---|---|---|
| Adaptive Intelligence (A) | Task success under shift | % success in changed conditions | >= 92% |  |  | AI Lead |  |
| Concord Alignment (C) | Concord pass rate | % decisions passing all 4 concord checkpoints | >= 95% |  |  | Governance Lead |  |
| Regenerative Resilience (R) | Recovery performance index | weighted MTTR + recovery quality score | >= 0.85 |  |  | Platform Lead |  |
| Groundedness (G) | Context-grounded action rate | % actions with high-confidence context validation | >= 93% |  |  | Domain SME |  |
| Operational Debt (D) | Drift + unresolved incidents index | normalized debt score | <= 0.15 |  |  | Program Lead |  |
| Human Oversight | Escalation appropriateness | % escalations aligned with policy severity | >= 97% |  |  | Risk Officer |  |
| Compliance | Policy exception rate | exceptions per 1,000 actions | <= 2.0 |  |  | Compliance |  |
| Trust & Adoption | Operator trust index | survey + behavior composite | >= 4.2/5 |  |  | Change Lead |  |

---

## B. DNAI Capability Index (Composite)

\[
\text{DNAI Capability Index} = (A \times C \times R \times G) - D
\]

**Scoring Guidance**
- Normalize A, C, R, G, D to a 0.00–1.00 scale.
- Use weighted normalization only when approved by governance board.
- Flag any period where one primary factor drops below 0.70.

---

## C. Operations Dashboard Template (Weekly)

### Panel 1: Concord Health
- Cognitive Concord pass/fail trend
- Context Concord confidence distribution
- Capability Concord denial categories
- Control Concord escalation volume

### Panel 2: Regeneration Health
- MTTR by incident class
- Auto-recovery success/fail ratio
- Repeat incident signatures
- Recovery quality degradation alerts

### Panel 3: Risk and Compliance
- Policy exceptions by severity
- Human override frequency and reason codes
- Open governance actions
- High-risk event timeline

### Panel 4: Domain Outcomes
- Domain KPI delta vs baseline
- Cost-to-outcome trend
- SLA performance
- Stakeholder confidence indicators

---

## D. Threshold Rules

- **Green**: All primary metrics at/above target; no critical incidents.
- **Yellow**: One primary metric out of range or elevated incident volume.
- **Red**: Two+ primary metrics out of range, any critical governance breach.

**Automatic Actions**
- Yellow: initiate constrained optimization sprint.
- Red: freeze scope expansion and trigger governance incident review.

---

## E. Governance Review Cadence

- Weekly operations review (engineering + domain)
- Biweekly risk review (governance + security + legal)
- Monthly steering review (executive sponsors)
- Quarterly recertification of Concord controls

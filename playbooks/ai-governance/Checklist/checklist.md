# Pre-Production AI Governance Checklist

Use before promoting any enterprise AI system from pilot to production.

## Ownership (RACI)

- [ ] **Review owner** assigned — who reviews AI outputs?
- [ ] **Escalation owner** assigned — who can pause the process?
- [ ] **Remediation owner** assigned — who coordinates fixes?
- [ ] **Communication owner** assigned — who informs the business?
- [ ] RACI matrix documented and signed off by sponsor

## Controls

- [ ] Human-in-the-loop defined for high-impact outputs
- [ ] Automated guardrails configured (input/output filtering)
- [ ] Audit logging enabled for all AI decisions
- [ ] Access controls reviewed (who can invoke, who can override)
- [ ] Data boundary documented (what data enters the model)

## Operations

- [ ] Incident runbook for AI failures written and tested
- [ ] Cost monitoring and budget alerts configured
- [ ] KPIs baselined (accuracy, latency, cost per inference, escalation rate)
- [ ] Rollback procedure documented
- [ ] On-call rotation includes AI system ownership

## Governance

- [ ] Governance audit dry-run completed
- [ ] Risk assessment updated for production scope
- [ ] Compliance review completed (if regulated industry)
- [ ] Stakeholder sign-off obtained

## Go / No-Go

| Criteria | Met? |
|----------|------|
| All ownership roles assigned | |
| Audit logging live | |
| Incident runbook tested | |
| Sponsor sign-off | |

**Decision:** Go / No-Go — Date: ___________ — Sponsor: ___________

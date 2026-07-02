# Implementation — AI Governance

## RACI matrix (template)

| Activity | Responsible | Accountable | Consulted | Informed |
|----------|-------------|-------------|-----------|----------|
| AI output review | ML Engineer | Product Owner | Legal | Business sponsor |
| Process pause / kill switch | Platform Eng | TPM | Security | Stakeholders |
| Incident remediation | On-call SRE | Engineering Manager | ML team | Business sponsor |
| Business communication | TPM | Product Owner | Legal, Comms | Executive sponsor |
| Governance audit | Compliance | CISO | TPM, ML | Board / Risk |

## Sample controls

### Audit logging

Log every AI inference with: timestamp, user, input hash, output summary, review status, model version.

### Human approval gate

High-impact outputs (financial, legal, customer-facing) require human approval before release. Define the threshold in your RACI.

### Cost monitoring

Set budget alerts per model endpoint. Track cost per inference and cost per business outcome.

## Runbook stub

1. **Detect** — monitoring alert or user report
2. **Triage** — on-call assesses severity (P1–P4)
3. **Pause** — escalation owner disables AI endpoint if needed
4. **Fix** — remediation owner coordinates model/data/prompt fix
5. **Communicate** — communication owner notifies stakeholders
6. **Post-mortem** — document root cause, update governance checklist

## Next: fill with your org's specifics

Replace template owners with actual names and teams. Add Terraform/K8s configs when your platform patterns are defined.

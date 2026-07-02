# Kryptunes — Enterprise AI Playbooks

**Practical implementation knowledge for enterprise AI leaders.**

Not a blog. Not opinions. Reusable frameworks, reference architectures, decision trees, and implementation guides for CIOs, CTOs, VPs of Engineering, and Platform Engineering leaders deploying AI in production.

→ [kryptunes.com](https://kryptunes.com) · [Insights](https://kryptunes.com/insights) · [LinkedIn](https://www.linkedin.com/in/consultkhalid/)

---

## Portfolio

| Playbook | Status | Focus |
|----------|--------|-------|
| [AI Governance](playbooks/ai-governance/) | **Live** | Pilot → production governance gap, RACI, human review, audit readiness |
| [AI Architecture](playbooks/ai-architecture/) | Planned | Reference architectures, integration patterns, model routing |
| [AI Operations](playbooks/ai-operations/) | Planned | Production monitoring, cost controls, SLOs, incident response |
| [AI Security](playbooks/ai-security/) | Planned | Security controls, data boundaries, prompt injection, access |
| [Agentic AI](playbooks/agentic-ai/) | Planned | Multi-agent patterns, delegation, human-in-the-loop |
| [Enterprise Case Studies](playbooks/enterprise-case-studies/) | Planned | Real deployment analyses |
| [Research](playbooks/research/) | Planned | Curated research notes with citations |

---

## Standard playbook layout

Every playbook follows the same structure — consistency reinforces the brand:

```
playbooks/<slug>/
├── README.md           Index + quick verdict
├── article.md          Decision framework / implementation guide (syncs to kryptunes.com/insights)
├── playbook.yaml       Sync metadata (Obsidian + Strapi)
├── Research/           Research notes, literature review
├── Architecture/       Diagrams, reference architectures (Mermaid)
├── Slides/             HTML decks + PNG exports
├── Implementation/     Sample configs, RACI, runbooks
├── Templates/          Reusable templates (ADRs, checklists)
├── Checklist/          Go-live and audit checklists
└── References/         Citations and source links
```

Copy `playbooks/_template/` to start a new playbook.

---

## Sync pipeline

| Target | What syncs | Command |
|--------|------------|---------|
| **GitHub** (this repo) | Source of truth — playbooks, slides, frameworks | `git push` |
| **Obsidian** | Vault notes under `20-29 KrypTunes/22 Platform/Enterprise AI Playbooks/` | `~/kxbrain/scripts/kryptunes-playbook-sync.py --playbook ai-governance` |
| **Strapi CMS** | `page_group: thoughts` → [kryptunes.com/insights](https://kryptunes.com/insights) | same command with `STRAPI_API_TOKEN` set |

See [sync/SYNC.md](sync/SYNC.md) for details.

---

## Positioning

> "This person understands how enterprise AI is actually deployed."

- Research-backed, not influencer commentary
- Implementation guides over hot takes
- Version-controlled frameworks recruiters and hiring managers can evaluate
- Consistent structure across every playbook

---

**Khalid Hossain** · TPM & Product Owner @ CGI · AI Researcher · Founder @ [Kryptunes](https://kryptunes.com)

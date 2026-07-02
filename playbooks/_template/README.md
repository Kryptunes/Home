# Playbook Template

Copy this folder to `playbooks/<your-slug>/` to start a new Enterprise AI playbook.

```bash
cp -r playbooks/_template playbooks/<your-slug>
```

## Required files

1. **README.md** — index with quick verdict table
2. **article.md** — decision framework (syncs to kryptunes.com/insights)
3. **playbook.yaml** — sync metadata for Obsidian + Strapi

## Standard folders

| Folder | Purpose |
|--------|---------|
| Research/ | Research notes, literature review |
| Architecture/ | Mermaid diagrams, reference architectures |
| Slides/ | HTML decks + PNG exports |
| Implementation/ | RACI, runbooks, sample configs |
| Templates/ | ADRs, checklists, decision records |
| Checklist/ | Go-live and audit checklists |
| References/ | Citations |

## Naming conventions

Use enterprise engineering language:

- ✅ Research Notes, Case Study, Reference Architecture, Decision Framework, Implementation Guide
- ❌ My Thoughts, Blog Post, Hot Take

## Sync

```bash
~/kxbrain/scripts/kryptunes-playbook-sync.py --playbook <your-slug>
```

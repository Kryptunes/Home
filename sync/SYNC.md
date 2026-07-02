# Sync — GitHub ↔ Obsidian ↔ Strapi

## Flow

```text
playbooks/<slug>/
  article.md       → GitHub only (implementation framework)
  strapi-post.md   → Strapi only (insights / traffic → kryptunes.com/insights)
  playbook.yaml    → metadata for both (separate titles)

Obsidian mirrors article.md (GitHub framework), not Strapi post.
```

## Commands (keep targets separate)

```bash
# GitHub: edit + git push (manual — source of truth for frameworks)

# Obsidian only (from article.md):
~/kxbrain/scripts/kryptunes-playbook-sync.py --playbook ai-governance --obsidian-only

# Strapi / insights only (from strapi-post.md):
~/kxbrain/scripts/kryptunes-playbook-sync.py --playbook ai-governance --strapi-only
```

## Prerequisites

| Target | Requirement |
|--------|-------------|
| GitHub | `gh auth login` (done on kxbrain) |
| Obsidian | Obsidian running; `OBSIDIAN_API_KEY` in `~/.hermes/.env` |
| Strapi | `STRAPI_API_TOKEN` in `~/.hermes/.env` |

### Add Strapi token

1. Strapi Admin → Settings → API Tokens → Create (Full access or custom with posts create/update)
2. Add to `~/.hermes/.env`:
   ```
   STRAPI_API_TOKEN=your-token-here
   ```

## Strapi mapping

| playbook.yaml field | Strapi field | Site route |
|---------------------|--------------|------------|
| `strapi_slug` | `slug` | `/insights/<slug>` |
| `page_group: thoughts` | `page_group` | Insights hub |
| `page_group: tech-pulse` | `page_group` | Tech & AI hub |
| `visibility: public` | `visibility` | Everyone |
| `article.md` body | `content` (HTML) | Post body |
| Slides PNG URL | `coverImageUrl` | Featured image |

## Obsidian mapping

| Source | Vault path |
|--------|------------|
| Hub index | `20-29 KrypTunes/22 Platform/Enterprise AI Playbooks.md` |
| Per playbook | `20-29 KrypTunes/22 Platform/Enterprise AI Playbooks/<Title>.md` |

Each playbook note links back to GitHub, Strapi insights URL, and LinkedIn caption draft.

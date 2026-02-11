# Thin Site Repo (Website Factory)

This repository is a **thin shell** for one website in the Website Factory portfolio.

## What lives here
- `content/` — generated pages (the asset)
- `data/site.yaml` — site identity, theme pack choice, hubs, generation rules
- `data/plan.yaml` — optional generation plan/queue
- `scripts/titles_pool.txt` — title inventory (generated/edited)
- `scripts/manifest.json` — duplicate prevention + run bookkeeping
- `.github/workflows/` — workflows that check out the core engine and generate content

## What does *not* live here
No layouts, CSS, or generator logic.

Those live in the public core repo:
- `deedsy1/website-factory-core`

## Hugo Modules
Layouts/assets are imported via Hugo Modules (see `hugo.yaml`). Cloudflare Pages will build this repo and fetch the core automatically.

## Running locally
1) Install Hugo Extended.
2) From this repo:
- `hugo server`

## Workflows
- **Bootstrap Site** (`bootstrap.yml`) generates site identity + titles pool + first pages.
- **Evergreen Factory** (`factory.yml`) generates pages on demand / schedule.

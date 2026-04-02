# CaptrID Help Centre (docs.captrid.com)

## What This Is
Public-facing documentation site for CaptrID, built with Mintlify. Deployed to docs.captrid.com.

## Product Repo
The product codebase lives at `C:\Users\Ben\Desktop\photo_capture_project`. Feature handovers, rules files, and database schema docs are the source of truth for what's implemented. This repo translates that into user-facing help content.

## Keeping Docs In Sync
`DOCS_MAP.md` tracks which docs pages correspond to which product features and when they were last synced. When updating a page, update the "Last Synced" date in the map.

## Writing Style
- **Tone**: Professional but friendly. Contractions ("you'll", "don't"), direct address ("Click **Save**")
- **Structure**: Requirements table up front → numbered steps → tips/warnings → troubleshooting table
- **Callouts**: `<Info>` for context, `<Tip>` for best practices, `<Warning>` for critical cautions
- **Screenshots**: `<Frame caption="..."><img src="/images/admin-guide/..." alt="..." /></Frame>` — placeholders are fine
- **UI references**: Bold for buttons and menu paths ("Go to **Organisation Settings** → **Billing**")
- **Cross-references**: `[Link Text](/path/to/page)` — always relative paths
- **Spelling**: Australian English (organisation, colour, licence)
- **Capitalisation**: Master List, Session, UID, Coordinator, Capturer — always capitalised as product terms

## Nav Config
`docs.json` controls sidebar navigation. Add new pages to the appropriate group. Groups:
- Getting Started
- Setting Up Your Organisation
- Managing Rosters (CSV, directory sync, SCIM)
- Running Sessions
- Syncing Data (changesets)
- ID Cards & Credentials
- Compliance & Data
- Capturer Guide
- More

## Key Commands
```bash
# Preview locally (requires Mintlify CLI)
mintlify dev

# Check for broken links
mintlify broken-links
```

# Docs ↔ Product Feature Map

When a product feature changes, check if the corresponding docs page needs updating.
When a handover doc is written, the docs update should be part of the same workflow.

## Mapping

| Docs Page | Product Source | Last Synced |
|-----------|---------------|-------------|
| `admin-guide/directory-sync.mdx` | Entra sync edge functions, `.claude/rules/module-directory-sync.md` | 2026-03-17 |
| `admin-guide/automated-provisioning.mdx` | SCIM edge function, `.claude/rules/module-scim.md`, `docs/handovers/SCIM_HANDOVER.md` | 2026-04-02 |
| `admin-guide/digital-cards.mdx` | Wallet pass edge functions, `.claude/rules/module-wallet-passes.md` | Unknown |
| `admin-guide/self-service-photo-upload.mdx` | Self-upload edge functions | Unknown |
| `admin-guide/plans-and-limits.mdx` | `admin/lib/pricing_config.dart`, `docs/strategy/PRICING_AND_GTM.md` | 2026-04-02 |
| `admin-guide/reviewing-photos.mdx` | Submissions service, approval RPC | Unknown |
| `admin-guide/saving-changes-to-master-list.mdx` | Changeset service | Unknown |
| `admin-guide/creating-a-session.mdx` | Sessions service, session wizard | Unknown |
| `admin-guide/session-templates.mdx` | Session templates service | Unknown |
| `admin-guide/importing-csv.mdx` | CSV import service | Unknown |
| `admin-guide/managing-master-lists.mdx` | Master list service | Unknown |
| `admin-guide/creating-card-templates.mdx` | Card design service | Unknown |
| `admin-guide/printing-id-cards.mdx` | Print engine, local print service | Unknown |
| `admin-guide/person-erasure.mdx` | `erase-person` edge function, erasure RPC | Unknown |
| `admin-guide/audit-logs.mdx` | `log_audit_event()` RPC | Unknown |
| `admin-guide/data-sessions.mdx` | Data session workflow | Unknown |
| `admin-guide/inviting-team-members.mdx` | `invite-user` edge function, user management service | Unknown |
| `admin-guide/organisation-settings.mdx` | Org settings, coordinator permissions | Unknown |
| `admin-guide/billing.mdx` | Stripe webhook, billing service | Unknown |

## "Unknown" = not yet audited

Run a docs review pass to fill in the "Last Synced" dates and flag any pages that have drifted.

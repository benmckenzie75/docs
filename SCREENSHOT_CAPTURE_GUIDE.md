# Screenshot Capture Guide for CaptrID Docs

## Capture Standards

### Browser Setup (Admin Portal)
- **Browser**: Chrome or Edge (consistent rendering across docs readers)
- **Window size**: Resize the actual browser window to **1440 x 900** (see below). This captures the full browser chrome at a consistent size.
- **Zoom**: 100% (no browser zoom)
- **Include in screenshot**: Full browser window — address bar, tab bar, and page content. This grounds the user in "this is a web app" and shows the URL.
- **Crop out**: Bookmarks bar (hide with Ctrl+Shift+B), extensions, OS taskbar. Just the browser window itself.
- **DevTools**: Closed
- **Dark mode**: Off — use light theme only
- **Tabs**: Only one tab open (the page being captured). No distracting other tabs.

#### Resizing the browser window
Use one of these to get a consistent 1440x900 browser window:
- **Chrome extension "Window Resizer"** — save a 1440x900 preset, resize with one click (recommended)
- **ShareX** (free) — Tools > Window resizer > set to 1440x900
- **PowerToys** — Window resizer utility built in

### Mobile App
- **Device**: Use a real device or simulator at standard resolution (iPhone 14/15 or Pixel 7)
- **Include device frame**: Yes — use a device mockup frame (Figma, CleanShot, or similar)
- **Orientation**: Portrait unless landscape is specifically needed
- **Status bar**: Include (shows time, signal, battery — makes it feel real)

### Image Specs
- **Format**: PNG (sharp text, no JPEG artefacts)
- **Max width**: 1200px (Mintlify renders at max ~800px, but 1200px gives retina sharpness)
- **Naming**: kebab-case, descriptive: `session-wizard-fields-step.png`, `master-list-csv-import-mapping.png`
- **Location**: Save all to `captrid-docs/images/` — use subfolders by section:
  ```
  images/
  ├── getting-started/
  ├── admin-guide/
  ├── capturer-guide/
  └── general/
  ```

### Data Quality
- **Use realistic demo data** — Australian names, real-looking student IDs, plausible year levels/houses
- **No real personal data** — Don't use actual customer data
- **Consistent org**: Use the same demo org throughout (e.g. "Riverside College")
- **Consistent people**: Reuse the same sample people across screenshots so it feels like one walkthrough
- **Clean state**: No error banners, no stale notifications, no half-finished test data

### Annotation
- **Don't annotate in the screenshots themselves** — Mintlify supports callouts and captions via `<Frame caption="...">`. Keep screenshots clean.
- **Exception**: If you need to highlight a specific button or area, use a subtle red/teal rounded rectangle outline (2px, no drop shadow). Never use arrows or numbered circles.

---

## Screenshot List by Page

### Getting Started > Quick Start (`getting-started/quick-start.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 1 | `getting-started/dashboard-empty.png` | Dashboard/home screen for a new org with no sessions yet | Before you begin | Shows the starting point — clean slate |
| 2 | `getting-started/sidebar-master-lists.png` | Sidebar with "Master Lists" highlighted | Step 1 | Crop to sidebar + just enough of the page to show context |
| 3 | `getting-started/create-master-list-dialog.png` | Create Master List dialog with name and fields filled in | Step 1 | Show a realistic name like "Students 2026" |
| 4 | `getting-started/master-list-with-people.png` | Master List detail screen with ~10 people showing | Step 1 | After import — shows the roster populated |
| 5 | `getting-started/session-wizard-type.png` | Session Wizard — Type step | Step 2 | Photo type selected |
| 6 | `getting-started/session-wizard-staff.png` | Session Wizard — Staff step with a capturer assigned | Step 3 | Show at least one capturer assigned |
| 7 | `getting-started/session-overview.png` | Session detail — Overview tab after creation | After creation | Shows the session is live, stats at zero |

### Getting Started > Key Concepts (`getting-started/key-concepts.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 8 | `getting-started/master-list-overview.png` | Master List detail screen showing schema + people | Master List | Show field columns, a few people, the toolbar |
| 9 | `getting-started/session-tabs.png` | Session detail screen showing the tab bar (Overview, Submissions, Roster, Staff, Card Design, Export) | Session | Capture wide enough to show all tabs |
| 10 | `getting-started/submission-statuses.png` | Submissions tab with a mix of pending, approved, rejected | Submission | Show the status badges clearly |
| 11 | `getting-started/changeset-review.png` | Changeset review screen showing a few items with session/master values | Saving to Master List | Show conflict resolution UI |
| 12 | `getting-started/card-designer-preview.png` | Card designer with a template and live preview showing real data | Card Templates | Show the 3-panel layout |

### Admin Guide > Inviting Team Members (`admin-guide/inviting-team-members.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 13 | `admin-guide/user-management-list.png` | User Management screen showing a few users with different roles | Managing existing users | Show role badges (Admin, Coordinator, Capturer) |
| 14 | `admin-guide/invite-user-dialog.png` | Invite User dialog with email filled in and role dropdown open | Inviting a user | Show all three role options in the dropdown |
| 15 | `admin-guide/coordinator-permissions.png` | Organisation Settings > Coordinator Permissions section | Coordinator permissions | Show the toggle switches with a couple enabled |

### Admin Guide > Plans and Limits (`admin-guide/plans-and-limits.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 16 | `admin-guide/billing-screen.png` | Billing screen showing current plan, usage bars, and upgrade button | Managing your subscription | Show realistic usage (not empty, not maxed) |

### Admin Guide > Importing CSV (`admin-guide/importing-csv.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 17 | `admin-guide/csv-upload-dialog.png` | CSV import — file upload step (file picker) | Importing into a Master List | Show the upload area |
| 18 | `admin-guide/csv-column-mapping.png` | CSV import — column mapping step showing auto-mapped + manually mapped fields | Importing into a Master List | Show CSV columns on left, Master List fields on right |
| 19 | `admin-guide/csv-import-preview.png` | CSV import — preview step showing first few rows | Importing into a Master List | Show the preview table with realistic data |
| 20 | `admin-guide/csv-import-results.png` | CSV import — results summary (created, updated, skipped counts) | What happens during import | Show a successful import summary |

### Admin Guide > Creating a Session (`admin-guide/creating-a-session.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 21 | `admin-guide/sessions-list.png` | All Sessions screen with a few sessions in different states (active, closed, archived) | Starting the wizard | Show the Create Session button prominently |
| 22 | `admin-guide/wizard-capture-mode.png` | Session Wizard — Capture Mode step showing the three options | Capture mode | Hybrid mode selected, Master List chosen as source |
| 23 | `admin-guide/wizard-fields.png` | Session Wizard — Fields step showing field list with UID, types, required toggles | Fields | Show a populated field list |
| 24 | `admin-guide/wizard-capturer-settings.png` | Session Wizard — Capturer Settings step showing visibility/edit/required toggles | Capturer settings | Show per-field toggle matrix |
| 25 | `admin-guide/wizard-export-settings.png` | Session Wizard — Export step showing filename template | Export settings | Show the filename template builder |
| 26 | `admin-guide/wizard-review.png` | Session Wizard — Review step showing full configuration summary | Review and create | Show all settings summarised |
| 27 | `admin-guide/session-detail-tabs.png` | Session detail screen showing all tabs after creation | After creation | Full-width, Overview tab active |

### Admin Guide > Reviewing Photos (`admin-guide/reviewing-photos.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 28 | `admin-guide/submissions-tab-pending.png` | Submissions tab filtered to Pending, showing photo thumbnails with person names | Viewing submissions | Show 6-8 pending submissions |
| 29 | `admin-guide/submission-detail-review.png` | Single submission detail — full photo, person info, Approve/Reject buttons | Reviewing a photo | Show the review actions clearly |
| 30 | `admin-guide/submission-reject-dialog.png` | Rejection dialog with reason text field | Rejection reasons | Show a filled-in reason like "Photo is blurry — please retake" |

### Admin Guide > Exporting (`admin-guide/exporting.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 31 | `admin-guide/export-tab.png` | Export tab showing export options (CSV, ZIP) and scope selection | Exporting photos | Show the main export interface |
| 32 | `admin-guide/export-history.png` | Export history section showing a few previous exports | Export history | Show dates, counts, who exported |

### Admin Guide > Saving Changes to Master List (`admin-guide/saving-changes-to-master-list.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 33 | `admin-guide/save-to-master-button.png` | Session Overview tab with "Save to Master List" button highlighted | Generating changes | Crop to just the relevant section |
| 34 | `admin-guide/changeset-summary.png` | Changeset summary showing counts: creates, updates, photo-only, conflicts | Generating changes | Show the summary badges |
| 35 | `admin-guide/changeset-item-detail.png` | Single changeset item showing session value vs master value with resolution options | Reviewing changes | Show a conflict with "Use session" / "Use master" buttons |
| 36 | `admin-guide/changeset-conflict.png` | A conflicted field showing both values side-by-side | Conflicts | Show clearly different values |
| 37 | `admin-guide/changeset-applied.png` | Changeset in "Applied" state with timestamp and rollback button | Applying changes | Show the applied state |

### Admin Guide > Card Templates (`admin-guide/creating-card-templates.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 38 | `admin-guide/card-templates-list.png` | Card Design screen showing a few templates with thumbnails | Creating a template | Show the template gallery |
| 39 | `admin-guide/card-designer-full.png` | Full card designer — left palette, centre canvas with a designed card, right properties panel | The card designer | This is the hero screenshot — make it look good |
| 40 | `admin-guide/card-designer-text-element.png` | Properties panel with a text element selected, showing variable dropdown | Using variables | Show `{{first_name}}` in the text content |
| 41 | `admin-guide/card-designer-preview.png` | Card preview with real person data (photo + name + ID) | Previewing with real data | Show the preview modal with navigation arrows |
| 42 | `admin-guide/card-designer-dual-sided.png` | Card designer showing front/back toggle | Dual-sided cards | Show the front/back switcher |
| 43 | `admin-guide/session-card-design-tab.png` | Session > Card Design tab showing linked templates with compatibility status | Session copies | Show "Compatible" badge |

### Capturer Guide > Capturing Photos (`capturer-guide/capturing-photos.mdx`)

These are **mobile screenshots** — use device frames.

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 44 | `capturer-guide/mobile-home-screen.png` | Mobile app home screen showing assigned sessions | Getting started | Show 1-2 sessions with names |
| 45 | `capturer-guide/mobile-person-list.png` | Person selection screen with roster, search bar, and status filters | Capturing a photo | Show the filter chips (Needs Photo, etc.) |
| 46 | `capturer-guide/mobile-camera-capture.png` | In-app camera with framing guide overlay and person name at top | Capturing a photo | Show the aspect ratio guide and rule-of-thirds grid |
| 47 | `capturer-guide/mobile-photo-review.png` | Photo review screen with quality check results | Capturing a photo | Show the validation badges (resolution OK, brightness OK, etc.) |
| 48 | `capturer-guide/mobile-crop-screen.png` | Crop screen with the aspect ratio enforced | Capturing a photo | Show the crop handles |
| 49 | `capturer-guide/mobile-offline-queue.png` | Offline queue showing queued photos with sync status | Working offline | Show the queue badge and "Sync Now" button |
| 50 | `capturer-guide/mobile-activity-tab.png` | Activity/submissions tab showing statuses | Photo statuses | Show a mix of pending, approved, rejected |
| 51 | `capturer-guide/mobile-data-session.png` | Data session capture screen showing form fields | Data sessions | Show editable fields + read-only fields |

### Support (`support.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 52 | `general/feedback-button.png` | The "Send Feedback" button/dialog in the admin portal | In-app feedback | Show the feedback form with type selector |

### Admin Guide > Managing Master Lists (`admin-guide/managing-master-lists.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 53 | `admin-guide/master-list-detail.png` | Master List detail screen showing schema fields and people list | Viewing a master list | Show field columns, toolbar, a few people with realistic data |
| 54 | `admin-guide/master-list-schema-editor.png` | Schema editor with field types, UID field marked | Editing the schema | Show the UID badge on the identifier field |
| 55 | `admin-guide/master-list-add-person.png` | Add Person dialog with fields filled in | Adding people manually | Show realistic Australian name and UID |

### Admin Guide > Digital Cards (`admin-guide/digital-cards.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 56 | `admin-guide/wallet-template-editor.png` | Wallet pass template editor with branding config | Creating a template | Show colour pickers, logo, card title fields |
| 57 | `admin-guide/wallet-pass-preview.png` | Pass preview showing branded card with photo | Previewing a pass | Show the Apple/Google Wallet preview with real person data |
| 58 | `admin-guide/wallet-generate-dialog.png` | Pass generation dialog with people selection | Generating passes | Show the people list with checkboxes |
| 59 | `admin-guide/wallet-passes-list.png` | Passes list showing different statuses (generated, distributed, installed, revoked) | Managing passes | Show status badges in different colours |

### Admin Guide > Self-Service Photo Upload (`admin-guide/self-service-photo-upload.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 60 | `admin-guide/self-upload-session-config.png` | Session config with email field and self-upload settings | Configuring self-upload | Show the email field dropdown and toggle |
| 61 | `admin-guide/self-upload-landing.png` | Subject's upload landing page (mobile frame) | The upload experience | Use a mobile device frame — show the branded upload page |
| 62 | `admin-guide/self-upload-invitation-status.png` | Admin view of invitation statuses | Monitoring progress | Show a mix of sent, opened, submitted statuses |

### Admin Guide > Directory Sync (`admin-guide/directory-sync.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 63 | `admin-guide/directory-connection-form.png` | Add Directory Connection form with tenant/client fields | Connecting a directory | Show Entra ID selected, tenant and client ID fields |
| 64 | `admin-guide/directory-field-mapping.png` | Field mapping wizard showing source to target mappings | Mapping fields | Show auto-mapped fields and a manual mapping |
| 65 | `admin-guide/directory-sync-results.png` | Sync results summary showing created/updated/deactivated counts | Running a sync | Show the results card with count badges |

### Admin Guide > Organisation Settings (`admin-guide/organisation-settings.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 66 | `admin-guide/org-settings-permissions.png` | Coordinator permissions section with toggle switches | Coordinator permissions | Show a couple of toggles enabled, others disabled |
| 67 | `admin-guide/org-settings-retention.png` | Data retention defaults section | Data retention | Show the retention policy dropdown and auto-archive toggle |

### Admin Guide > Printing ID Cards (`admin-guide/printing-id-cards.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 68 | `admin-guide/print-wizard-template.png` | Print Wizard template selection step | Choosing a template | Show template cards with thumbnails |
| 69 | `admin-guide/print-wizard-people.png` | People selection with readiness indicators | Selecting people | Show readiness icons (green tick, amber warning) |
| 70 | `admin-guide/print-wizard-preview.png` | Card preview with real person data | Previewing cards | Show the rendered card with photo and field values |

### Admin Guide > Data Sessions (`admin-guide/data-sessions.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 71 | `admin-guide/data-session-wizard.png` | Session Wizard with Data type selected | Creating a data session | Show the type step with Data radio selected |
| 72 | `admin-guide/data-review-queue.png` | Data review queue showing submission statuses | Reviewing data submissions | Show a mix of Pending, Approved statuses |

### Admin Guide > Audit Logs (`admin-guide/audit-logs.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 73 | `admin-guide/audit-logs-list.png` | Audit log list with recent entries | Viewing the log | Show a few rows with action, entity, user, timestamp |
| 74 | `admin-guide/audit-logs-filters.png` | Filter controls (entity type, action, date range) | Filtering logs | Show the filter dropdowns expanded or with selections |

### Admin Guide > Person Erasure (`admin-guide/person-erasure.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 75 | `admin-guide/person-erasure-search.png` | Search results grouped by UID with expandable details | Searching for a person | Show expanded card with per-source field data |
| 76 | `admin-guide/person-erasure-preview.png` | Dry-run preview dialog showing deletion counts | Previewing erasure | Show the counts (master list records, session records, submissions) |

### Admin Guide > Session Templates (`admin-guide/session-templates.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 77 | `admin-guide/session-templates-list.png` | Templates list screen with template cards | Viewing templates | Show a few template cards with names and descriptions |
| 78 | `admin-guide/session-wizard-template-dropdown.png` | Session Wizard with template dropdown open | Using a template | Show the dropdown expanded with template options |

### Admin Guide > Your Account (`admin-guide/managing-your-account.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 79 | `admin-guide/profile-page.png` | Profile page showing avatar, name, email, organisations | Your profile | Show realistic user info and org membership |

### Admin Guide > Billing (`admin-guide/billing.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 80 | `admin-guide/billing-usage.png` | Billing screen with usage bars and current plan | Current usage | Show realistic usage levels (not empty, not maxed) |
| 81 | `admin-guide/billing-plan-cards.png` | Plan comparison cards | Comparing plans | Show Starter, Pro, Business cards with feature lists |

### Admin Guide > Dashboard (`admin-guide/dashboard.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 82 | `admin-guide/dashboard-welcome.png` | Dashboard top section with welcome banner and stats | Dashboard overview | Show welcome message and summary stat cards |
| 83 | `admin-guide/dashboard-priority-inbox.png` | Priority inbox with action items | Priority inbox | Show a few actionable items (pending reviews, expiring sessions) |

### Admin Guide > Analytics (`admin-guide/analytics.mdx`)

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 84 | `admin-guide/analytics-overview.png` | Analytics Overview tab with summary cards | Overview metrics | Show the summary cards with realistic numbers |
| 85 | `admin-guide/analytics-trends.png` | Trends tab with daily submissions chart | Trends | Show the chart with data points over a few weeks |

### Capturer Guide > Data Entry (`capturer-guide/data-entry.mdx`)

These are **mobile screenshots** — use device frames.

| # | Filename | What to capture | Section | Notes |
|---|----------|----------------|---------|-------|
| 86 | `capturer-guide/mobile-data-entry-form.png` | Data entry form on mobile (mobile frame) | Entering data | Show editable fields with realistic values |
| 87 | `capturer-guide/mobile-revision-notes.png` | Revision notes banner on mobile (mobile frame) | Revision notes | Show the amber revision notes banner with admin feedback |

---

## Capture Checklist

### Before You Start
- [ ] Set up a demo org "Riverside College" with realistic data
- [ ] Create a Master List "Students 2026" with ~20 people (Australian names)
- [ ] Import via CSV so you have that flow ready
- [ ] Create a session "Photo Day — March 2026" from the Master List
- [ ] Assign at least one capturer
- [ ] Submit a few photos (some pending, some approved, some rejected)
- [ ] Create a card template with a decent design
- [ ] Generate a changeset with at least one conflict
- [ ] Have the mobile app ready with the same session

### Capture Order (Efficiency)
Capture in this order to minimise setup/navigation:

1. **Dashboard** (empty state, populated, welcome banner, priority inbox)
2. **Master Lists** screens (list, detail, schema editor, add person, CSV import flow)
3. **Session Templates** (list, wizard dropdown)
4. **Sessions** screens (list, wizard steps 1-8, detail tabs, data session wizard)
5. **Submissions** screens (list, detail, reject dialog, data review queue)
6. **Export** tab
7. **Changeset** screens (generate, review, conflict, applied)
8. **Card Design** screens (list, designer, preview, session tab)
9. **Wallet Passes** screens (template editor, preview, passes list, generation dialog)
10. **Print Wizard** screens (template selection, people selection, card preview)
11. **User Management** screens (list, invite dialog)
12. **Organisation Settings** (coordinator permissions, retention defaults)
13. **Billing** screen (plan cards, usage bars)
14. **Analytics** (overview, trends)
15. **Person Erasure** (search results, preview dialog)
16. **Audit Logs** (list, filters)
17. **Profile** (account page)
18. **Directory Sync** screens (connection form, field mapping, sync results)
19. **Self-Service Upload** screens (session config, landing page, invitation statuses)
20. **Feedback** dialog
21. **Mobile app** screens (home, roster, camera, review, crop, queue, activity, data session, data entry form, revision notes)

### Tools
- **macOS**: CleanShot X (crop, device frames, scrolling capture)
- **Windows**: ShareX (free, crop, annotations) or Snagit
- **Browser**: Chrome DevTools device toolbar for consistent viewport (Ctrl+Shift+M → set to 1440x900)
- **Mobile frames**: Use https://mockuphone.com or Figma device frames
- **Batch resize**: Use `sips` (macOS) or ImageMagick to ensure all PNGs are max 1200px wide

### Quick Capture Workflow
1. Resize browser window to 1440x900 (use Window Resizer extension or ShareX)
2. Hide bookmarks bar (Ctrl+Shift+B), close other tabs
3. Navigate to the screen
4. Clean up any test data or errors
5. Screenshot the full browser window (Win+Shift+S > Window capture, or ShareX > Window)
6. Save as PNG to the correct `images/` subfolder
7. Name using the convention above

---

## Mintlify Image Usage

Once captured, add to `.mdx` files like this:

```mdx
<Frame caption="The Session Wizard guides you through setup in a few steps">
  <img src="/images/admin-guide/wizard-fields.png" alt="Session Wizard fields step" />
</Frame>
```

For side-by-side comparisons:
```mdx
<Columns cols={2}>
  <Frame caption="Before: Pending submissions">
    <img src="/images/admin-guide/submissions-tab-pending.png" alt="Pending submissions" />
  </Frame>
  <Frame caption="After: Approved submissions">
    <img src="/images/admin-guide/submissions-tab-approved.png" alt="Approved submissions" />
  </Frame>
</Columns>
```

For mobile screenshots (smaller display):
```mdx
<Frame caption="The in-app camera with framing guide">
  <img src="/images/capturer-guide/mobile-camera-capture.png" alt="Mobile camera capture" style={{maxWidth: '300px'}} />
</Frame>
```

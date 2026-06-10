# Octus ESG Intelligence Agent

Internal AI-powered operations tool for the Octus London ESG team.

Built on Claude.ai Enterprise · Tier 2 Team Application · Not customer-facing

---

## What this is

The ESG Intelligence Agent is an internal copilot for the Octus ESG Operations and Delivery team in London. It connects to the shared `esg@octus.com` inbox, monday.com workflow boards, and ESG methodology resources to help the team triage client queries, manage SFDR reporting cycles, track regulatory signals, and draft responses — faster and with full audit trails.

It is built as a single HTML artifact running inside Claude.ai Enterprise, using the Anthropic API and MCP connectors for Gmail, monday.com, Google Drive, and Slack.

---

## Application tier

| Property | Value |
|---|---|
| Tier | 2 — Team |
| Built by | ESG London team (with Claude) |
| Used by | ESG London team (internal only) |
| Supported by | Seyi Khalidson (owner) |
| Customer-facing | Never |
| IT registration | Required before team rollout |
| Security review | Partial (IT notified, information barriers enforced) |

Per the Octus Application Tiers framework. See IT for the full policy.

---

## Team

| Name | Role | Tab ownership |
|---|---|---|
| Seyi Khalidson | ESG Ops & Delivery · Project owner | Inbox, architecture |
| Caterina Dassie | ESG Operations Lead | Review, Clients tab |
| Niamh Trinci | ESG Ops & Delivery | Workflow tab |
| Scott Plumridge | ESG Ops & Delivery | Workflow tab |
| Luca Strada | ESG Ops & Delivery | Signals tab |
| Alina Simion | Senior ESG Analyst | Signals tab, methodology |

---

## Tabs and status

| Tab | Status | Description |
|---|---|---|
| Inbox | ✅ Live | Gmail MCP triage with AI briefs, four categories, draft responses |
| Workflow | 🔲 Skeleton | monday.com ESG Workflow Dashboard integration |
| Signals | 🔲 Skeleton | Regulatory feed — ESMA, EU Commission, IFRS, CDP |
| Clients | 🔲 Skeleton | Client profiles from monday.com Clients board |
| Files | 🔲 Skeleton | Drive, SharePoint, OneDrive unified search |
| Audit log | ✅ Live | Full read/write/confirm/error log, JSON and CSV export |

---

## Connectors

| Connector | Used for | Status |
|---|---|---|
| Gmail MCP | esg@octus.com shared inbox | Live |
| monday.com MCP | Client lookup during triage | Live (partial) |
| Google Drive MCP | Methodology and file search | Planned |
| Slack MCP | Team coordination | Planned |
| Anthropic API | Brief generation, draft writing | Live |

---

## How to run

1. Open Claude.ai Enterprise and navigate to the **Octus ESG Intelligence Agent** shared Project
2. Open the latest artifact (`octus-esg-agent.html`) from the conversation
3. The inbox loads automatically — Gmail MCP connects if authorised, otherwise demo mode activates
4. For standalone preview: download the HTML file and open in any browser — demo mode only

No servers. No deployment. No infrastructure required at Tier 2.

---

## How to contribute

### Using Claude.ai Enterprise (primary workflow)
1. Open the shared Project in Claude.ai Enterprise — all team members have access
2. Start a new conversation inside the project
3. Tag the tab you are working on in your first message (e.g. "Working on the Workflow tab")
4. Test your changes in the artifact preview
5. When stable, download the HTML and commit to this repo

### Using GitHub (version control)
1. Clone the repo: `git clone https://github.com/octus-intelligence/octus-esg-intelligence-agent`
2. Create a branch for your tab: `git checkout -b tab/workflow-niamh`
3. Make changes to `octus-esg-agent.html`
4. Commit with a clear message: `git commit -m "workflow: add kanban view from monday board"`
5. Open a pull request against `main` — Seyi reviews and merges

### Branch naming convention
- `tab/inbox-*` — Inbox tab changes
- `tab/workflow-*` — Workflow tab
- `tab/signals-*` — Signals tab
- `tab/clients-*` — Clients tab
- `tab/files-*` — Files tab
- `fix/*` — Bug fixes
- `infra/*` — Architecture or connector changes

---

## Information barriers

Per the Octus Compliance Manual and Application Tiers framework:

- Each team member runs the agent against their own Claude.ai account
- `window.storage` is per-user — no cross-user state
- Email bodies are never persisted — only generated briefs and audit metadata
- MNPI handling: the agent does not surface Private-side data to Public-side users
- Audit log is exportable per user for compliance retention

---

## Versioning

| Version | Date | Notes |
|---|---|---|
| v1.0 | May 2026 | Inbox tab live, three-panel layout, Gmail MCP, demo mode |

---

## Contacts

**Project owner:** Seyi Khalidson — seyi.khalidson@octus.com
**ESG Lead:** Caterina Dassie — caterina.dassie@octus.com
**IT registration contact:** Umesh Pokhrel
**Compliance questions:** David Barker (Head of Information Security)

---

*Octus Intelligence · Internal use only · Not for redistribution · Not customer-facing*

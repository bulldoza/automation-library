# n8n-workflows

All n8n workflow exports for the automation hub. Each subfolder groups workflows by purpose or client.

## Subfolders

| Folder | Purpose |
|---|---|
| `lead-capture/` | Lead intake, form submissions, CRM sync workflows |
| `ai-agents/` | AI-powered agent workflows (OpenAI, Anthropic, etc.) |
| `rag/` | Retrieval-augmented generation pipelines (vector DB ingestion, Q&A) |
| `callguard/` | CallGuard missed-call and follow-up automation |
| `templates/` | Generic reusable workflows — no client-specific data |
| `clients/` | One folder per client containing their workflows |

## File Naming Convention

```
[client-or-category]_[short-description]_v[version].json
```

Examples:
```
lead-capture_webhook-to-crm_v1.json
bagups_abandoned-cart-followup_v2.json
template_slack-error-alert_v1.json
callguard_missed-call-sms_v3.json
```

Rules:
- All lowercase
- Hyphens within a segment, underscores between segments
- Always include a version suffix (`_v1`, `_v2`, …)
- Export from n8n via: **Workflow → Download** (saves as `.json`)

## Exporting from n8n

1. Open the workflow in n8n
2. Click the three-dot menu (top right) → **Download**
3. Save the `.json` into the correct subfolder here
4. Commit with a message like: `feat(n8n): add bagups lead-capture webhook v1`

## Client Folders

```
clients/
├── malosteel/
├── bagups/
├── cleaning-business/
└── c4-auto-detail/
```

Add a new client folder when you start work for a new client. Keep one workflow per file — do not bundle multiple workflows into one export unless they are a single n8n workflow.

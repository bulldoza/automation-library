# 05-Automation

Central automation development hub. This repo organizes n8n workflows, AI agents, RAG pipelines, Flowise projects, client automations, prompts, and documentation.

## Folder Structure

```
05-Automation/
├── n8n-workflows/          # All n8n workflow exports (.json)
│   ├── lead-capture/       # Lead gen and intake workflows
│   ├── ai-agents/          # AI agent workflows
│   ├── rag/                # Retrieval-augmented generation pipelines
│   ├── callguard/          # CallGuard-specific workflows
│   ├── templates/          # Reusable workflow templates
│   └── clients/            # Per-client workflow folders
│       ├── malosteel/
│       ├── bagups/
│       ├── cleaning-business/
│       └── c4-auto-detail/
│
├── flowise/                # Flowise chatflow exports and configs
├── prompts/                # System prompts, agent instructions, prompt templates
├── documentation/          # Guides, SOPs, architecture notes
├── screenshots/            # UI screenshots for documentation
├── archive/                # Deprecated or inactive workflows (do not delete)
│
├── automation-library/     # Separate git repo (github.com/bulldoza/automation-library)
├── chatbot/                # Standalone chatbot project
└── workflows/              # Legacy folder — migrate contents to n8n-workflows/ over time
```

## Naming Conventions

### Workflow files
```
[client-or-category]_[short-description]_v[version].json
```
Examples:
- `bagups_lead-capture-form_v1.json`
- `callguard_missed-call-followup_v2.json`
- `template_email-notification_v1.json`

### Client folders
Use lowercase, hyphen-separated names matching the client slug. One subfolder per client under `n8n-workflows/clients/`.

### Versioning
Increment `v1 → v2` when a workflow has breaking changes. Use git history for minor revisions — don't duplicate files with minor-version suffixes.

### Archiving
When retiring a workflow, move it to `archive/` with a dated prefix:
```
2025-06-05_bagups_old-lead-form_v1.json
```

## Related Repos

- [automation-library](https://github.com/bulldoza/automation-library) — reusable automation components

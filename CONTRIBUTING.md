# Contributing

Thank you for helping expand the n8n Workflows collection!

## Workflow Folder Format
workflows/<category>/<workflow-slug>/
├─ workflow.json # Export from n8n
└─ README.md # Use the template in /templates
## Workflow README should include:
- Purpose / overview
- Required credentials
- Setup instructions
- Optional: diagrams or screenshots

## How to export from n8n:
1. Open the workflow in your n8n editor.
2. Click the **three dots menu** (⋮) → **Download**.
3. Save the `.json` and place it in the correct folder.

## Guidelines:
- Use clear slugs (e.g., `gmail-new-subscriber-welcome`).
- Keep credentials out of JSON and screenshots.
- Test before submitting a PR.

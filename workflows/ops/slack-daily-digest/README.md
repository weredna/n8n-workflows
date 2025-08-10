# Slack Daily Digest

**Category:** ops  
**Summary:** Post a daily Slack digest of items added to a Google Sheet in the last 24 hours.  
**Apps/Nodes:** Schedule Trigger → Google Sheets (Read) → Code → Slack  
**Tags:** #n8n #slack #sheets #digest #ops

## 🧰 What this workflow does
- Triggers every day at a set time.
- Reads rows from a Sheet (e.g., `Daily Tasks`).
- Filters rows where `CreatedDate` is within the last 24 hours.
- Posts a formatted list to a Slack channel.

## 📦 Requirements
- Google credentials (Sheets)
- Slack credentials (Bot token)
- Sheet with at least: `Task`, `Owner`, `DueDate`, `CreatedDate` (ISO or yyyy-mm-dd)

## ⚙️ Setup
1. Set your **Schedule Trigger** time.
2. Point **Google Sheets** node to your `Daily Tasks` sheet & range (`Tasks!A:D`).
3. Update Slack **Channel** in the Slack node.
4. Activate the workflow.

## 🧪 Example row
| Task                | Owner | DueDate    | CreatedDate |
|---------------------|-------|------------|-------------|
| Approve budget plan | Alex  | 2025-08-15 | 2025-08-10T08:22:00Z |

## 🛠 Troubleshooting
- If the digest is empty, check date formats and timezone assumptions in the Code node.
- Long messages may be truncated by Slack; consider uploading a file when very long.

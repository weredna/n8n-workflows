# Forms to Notion

**Category:** content  
**Summary:** Save each new Google Forms response to a Notion database.  
**Apps/Nodes:** Google Sheets Trigger (linked Form responses) → Notion  
**Tags:** #n8n #notion #forms #database #content

## 🧰 What this workflow does
- Triggers when a new response is added to the **Form Responses** sheet.
- Creates a new page in a Notion database with mapped properties.

## 📦 Requirements
- Google credentials (Sheets)
- Notion credentials + a database (and the integration invited to it)
- Linked Google Form → Google Sheet

## ⚙️ Setup
1. In Google Forms, link responses to a Google Sheet (default tab `Form Responses 1`).
2. In Notion, create a database with properties: `Name` (Title), `Email` (Email), `Feedback` (Rich text).
3. In n8n, set credentials and update:
   - **Google Sheets Trigger** → `sheetId`, `range` (e.g., `Form Responses 1!A:C`)
   - **Notion** node → `databaseId`
4. Activate and submit a test Form.

## 🧪 Example fields
Name: Taylor R
Email: taylor@example.com
Feedback: Love the new product design

## 🛠 Troubleshooting
- If Notion errors on properties, double-check property **types** and names.
- Ensure your Notion integration is **invited** to the database.

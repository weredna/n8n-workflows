# Gmail: New Subscriber Welcome

**Category:** marketing  
**Summary:** Send a personalized welcome email when a new subscriber is added to the Google Sheets **Subscribers** sheet.  
**Apps/Nodes:** Google Sheets Trigger → Gmail  
**Tags:** #n8n #gmail #sheets #welcome #email

## 🧰 What this workflow does
- Triggers on **new row** in `Subscribers!A:B`.
- Sends a **Gmail** email using `Email` and `FirstName` columns.

## 📦 Requirements
- Google credentials for Sheets and Gmail (OAuth2 in n8n)
- A Sheet named **Subscribers** with columns: `Email`, `FirstName`

## ⚙️ Setup
1. In Google Sheets, create `Subscribers` with columns `Email`, `FirstName`.
2. In n8n, set credentials for **Google** (Sheets) and **Gmail**.
3. Open the workflow and set:
   - **Google Sheets Trigger** → `sheetId` and `range` (`Subscribers!A:B`)
4. Activate the workflow and add a test row.

## 🧪 Example row
Email: andrew@andrewluxem.com
FirstName: Andrew

## 🛠 Troubleshooting
- If it doesn’t trigger, verify the **sheet ID**, **range**, and that your creds are connected.
- Gmail daily send limits apply (depending on your account type).

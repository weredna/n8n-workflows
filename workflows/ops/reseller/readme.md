# Reseller Anon Workflow

**Category**: ecommerce  
**Summary**: Automates the analysis of resale items based on image input and price, providing a buying verdict for resellers.

**Apps/Nodes**:  
- n8n  
- OpenAI  
- Discord  

**Tags**: #n8n #automation #reselling #AI #ecommerce

---

### 🧰 What this workflow does

This workflow analyzes images of resale items, extracts price and brand details, and returns a verdict on whether to buy or pass based on estimated profit. The result is sent to a Discord channel for review.

### Step 1: Trigger the Webhook  
The workflow is triggered when a new message with an image is posted to a specific Discord channel. The message content includes the item price and brand.

### Step 2: Process the Image  
The image is sent to OpenAI for analysis, where the item’s details are extracted and evaluated.

### Step 3: Send Results to Discord  
The analysis results, including item name, price, estimated profit, and buying verdict, are sent back to the Discord channel for review.

---

### 📦 Requirements

- **n8n instance**  
- **OpenAI account** for image analysis  
- **Discord Bot** for sending results to a server  
- **Webhook URL** to trigger the workflow  
- **Custom credentials** for OpenAI and Discord Bot APIs

---

### ⚙️ Setup

1. Import the `workflow.json` file into your n8n instance.
2. Configure credentials in the following nodes:
   - OpenAI API (Replace with your API key)
   - Discord Bot API (Replace with your bot token)
   - Webhook URL (Replace with your specific URL)
3. Adjust filters, mappings, or schedules as needed.
4. Activate the workflow to start automation.

---

### 🧪 Example Data

**Example Trigger Payload** (Webhook):
```json
{
  "username": "resellerUser",
  "content": "$6.99 brand: alembika",
  "attachments": [
    "https://cdn.discordapp.com/attachments/1391621196667424778/1394092419451981938/PXL_20250710_200907848.jpg"
  ],
  "timestamp": "2025-07-13T23:05:33.842Z"
}

### Example Output

{
  "itemName": "Alembika Dress",
  "category": "Fashion",
  "eBayPrice": "$45.99",
  "FBMPPrice": "$38.50",
  "estimatedProfit": "$12.50",
  "verdict": "✅ Buy"
}


### Troubleshooting
Issue: Image analysis not triggering.
Solution: Ensure the webhook URL is correctly configured, and the trigger data is properly formatted with an image attachment.

Issue: API errors from OpenAI.
Solution: Check the OpenAI API key and ensure that your account has sufficient quota.

Issue: Incorrect item data or missing fields.
Solution: Review the Code nodes where data is extracted and ensure the input message matches the expected format.

### Notes:
- **Webhook URL** and **API credentials** are placeholders for your specific setup.
- Add a **workflow diagram** if available, or remove the section if you don't plan to use it.

This README is formatted for easy sharing and to provide clear instructions for anyone looking to implement or modify the workflow.

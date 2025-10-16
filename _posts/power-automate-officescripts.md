---
layout: post
title: Running OfficeScripts in Power Automate
date: 2025-10-16 15:45:00 -0500
category: Power Automate
---
## Can I enter OfficeScripts directly into PowerAutomate or can PowerAutomate only run OfficeScripts created in Excel?

No, you cannot write or edit Office Scripts directly inside Power Automate.
Power Automate can only run Office Scripts that were created and saved in Excel on the web (Excel for Microsoft 365) and stored in OneDrive for Business.

## How It Works
1. Office Scripts are authored in Excel on the web:
- You write them using the Code Editor in Excel (JavaScript/TypeScript-based).
- Scripts are saved to your OneDrive for Business under your account.
2. Power Automate accesses these scripts via the "Run script" action:
- Trigger: Any (manual, scheduled, file-based, etc.)
- Action: Excel Online (Business) > Run script
- You select:
  - The workbook (must be in OneDrive or SharePoint)
  - The script (from that workbook)
  - Any parameters the script expects
3. Scripts must already exist in the workbook.

## 🔒 Why This Limitation Exists
- Office Scripts are tightly integrated with Excel’s object model.
- They require the Excel workbook context to compile and validate the script.
- Power Automate is just the orchestrator — it doesn’t host or interpret the script code itself.

## 🛠️ How to Use Office Scripts in Power Automate
1. Open Excel on the web.
2. Go to **Automate** > **New Script**.
3. Write your script and save it.
4. In Power Automate:
- Use the **Run script** action.
- Point to the workbook and script.
- Pass any required parameters.

## 🧩 Combining with Other Actions
You can chain Office Scripts with other Power Automate actions like:
- Moving files
- Sending emails
- Updating SharePoint lists
- Triggering based on file creation or modification

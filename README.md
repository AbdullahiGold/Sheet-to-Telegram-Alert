[README (7).md](https://github.com/user-attachments/files/31235930/README.7.md)
# Sheet to Telegram Alert

> Watches a Google Sheet for new rows and sends an instant Telegram alert when one appears.

An [n8n](https://n8n.io/) workflow, built and run in production.

## What it does

Polls a Google Sheet every minute using n8n's Google Sheets Trigger (row-added event) and forwards the new row's data as a Telegram message. Pairs naturally with the Form Submission to Sheets workflow — together they form a form → sheet → instant-alert pipeline with no manual checking required.

**Why I built it:** Wanted to know the moment someone filled out my form, instead of checking the sheet manually.

## Trigger

Google Sheets Trigger (poll every minute, row added)

## Nodes used

- Google Sheets Trigger
- Telegram

## Setup

1. Import `Sheet-to-Telegram Alert.json` into n8n.
2. In the **Google Sheets Trigger** node, replace `YOUR_GOOGLE_SHEET_ID` with your own sheet and connect your Google Sheets Trigger credential.
3. In the **Send a text message** node, replace `YOUR_TELEGRAM_CHAT_ID` with your own chat ID and connect your Telegram bot credential.
4. Activate the workflow.

> Credentials (Gmail, Google Sheets, Telegram, etc.) are never included in exported workflow JSON — you'll need to connect your own in the n8n UI after import.

## Files

- [`Sheet-to-Telegram Alert.json`](Sheet-to-Telegram%20Alert.json) — the exported n8n workflow, ready to import

---

Suggested repo topics: `n8n, automation, telegram-bot, google-sheets, real-time-alerts, notifications`

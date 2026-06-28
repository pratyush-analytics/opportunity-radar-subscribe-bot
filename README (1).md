# 🤖 Opportunity Radar — Subscribe Bot

> A Telegram bot that automatically collects subscriber details and adds them to the daily digest system.

![n8n](https://img.shields.io/badge/Built%20with-n8n-orange) ![Telegram](https://img.shields.io/badge/Bot-Telegram-blue) ![Google Sheets](https://img.shields.io/badge/Storage-Google%20Sheets-green)

---

## 🧠 What It Does

1. **Listens** for any message on Telegram
2. **Checks** if the user is already subscribed
3. **Collects** Name + Email via an interactive form
4. **Saves** subscriber details to Google Sheets
5. **Confirms** subscription with a welcome message

---

## 🔄 Flow

```
User messages bot
      ↓
Find Subscriber (check if exists)
      ↓
Already Subscribed?
  ↓ YES                    ↓ NO
Tell Already          Ask Name & Email (form)
Subscribed                  ↓
                     Save to Google Sheets
                            ↓
                    Send Confirmation Message
```

---

## 🛠️ Tech Stack

- **n8n Cloud** — Workflow automation
- **Telegram Bot API** — User interaction
- **Google Sheets** — Subscriber storage

---

## 🔑 Credentials Required

| Service | Where to Get |
|---|---|
| Telegram Bot Token | @BotFather on Telegram |
| Google Sheets OAuth2 | Google Account Settings |

---

## 📥 How to Import in n8n

1. Open [n8n Cloud](https://app.n8n.cloud)
2. Click **New Workflow**
3. Click **⋯ menu** → **Import from file**
4. Select `opportunity-radar-subscribe-bot.json`
5. Add your Telegram and Google Sheets credentials
6. Update Google Sheet ID in the **Save Subscriber** node
7. Toggle **Active** → ON

---

## 📋 Nodes

| # | Node | Purpose |
|---|---|---|
| 1 | On Telegram Message | Listens for any Telegram message |
| 2 | Find Subscriber | Checks if chat_id already exists |
| 3 | Check If Found | Code node to evaluate result |
| 4 | Already Subscribed? | IF branch |
| 5 | Tell Already Subscribed | Sends info message to existing user |
| 6 | Ask Name And Email | Sends interactive form to new user |
| 7 | Save Subscriber | Appends details to Google Sheets |
| 8 | Send Confirmation | Sends welcome confirmation |

---

## 🤝 Pair With

👉 [opportunity-radar-ai](https://github.com/pratyush-analytics/opportunity-radar-ai) — Main digest workflow

---

## 👨‍💻 Author

**Pratyush Gupta** — [@pratyush-analytics](https://github.com/pratyush-analytics) — Chandigarh University

*Built as Project B — AI Agent Development Assignment*

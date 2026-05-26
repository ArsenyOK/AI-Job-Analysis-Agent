# AI Job Analysis Agent

AI-powered automation workflow built with n8n.

Features:

- Automatic job scraping
- HTML cleaning
- AI job analysis
- Match scoring
- Cover letter generation
- Google Sheets integration
- Telegram notifications

Stack:

- n8n
- OpenAI
- Google Sheets API
- Telegram Bot API
- Docker

Architecture:
Google Sheets
→ HTTP Request
→ HTML Parsing
→ OpenAI
→ JSON Parsing
→ Google Sheets Update
→ Telegram Notification

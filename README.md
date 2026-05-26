# AI Job Analysis Agent

AI-powered job analysis and automation workflow built with n8n, OpenAI, Google Sheets, and Telegram.

The system automatically:

- detects new job URLs,
- scrapes job pages,
- extracts and cleans HTML,
- analyzes jobs with AI,
- calculates job match percentage,
- generates AI cover letters,
- updates Google Sheets,
- sends Telegram notifications.

---

# Features

- Automatic job scraping
- HTML cleaning & extraction
- AI job analysis
- Match scoring
- AI-generated cover letters
- Google Sheets integration
- Telegram notifications
- Automated workflow execution
- Dockerized local setup

---

# Stack

- n8n
- OpenAI API
- Google Sheets API
- Telegram Bot API
- Docker
- JavaScript (n8n Code nodes)

---

# Architecture

Google Sheets
→ HTTP Request
→ HTML Parsing
→ OpenAI
→ JSON Parsing
→ Google Sheets Update
→ Telegram Notification

---

# Requirements

Before starting:

- Docker Desktop installed
- OpenAI API Key
- Telegram Bot Token
- Google Sheets API credentials

---

# Installation

## 1. Clone repository

```bash
git clone https://github.com/YOUR_USERNAME/ai-job-analysis-agent.git

cd ai-job-analysis-agent
```

---

## 2. Create .env file

Copy and fill out the file:

```bash
cp .env.example .env
```

---

## 3. Start n8n

```bash
docker compose up -d
```

---

## 4. Open n8n

```txt
http://localhost:5678
```

---

# Import Workflow

Inside n8n:

1. Click:
   `Import from File`

2. Select:

```txt
workflows/ai-job-analysis-agent.json
```

3. Configure credentials:

- OpenAI
- Google Sheets
- Telegram

4. Activate workflow

---

# Google Sheets Structure

Example columns:

| ID  | Job URL | Company | Position | Match % | Recommendation | Cover Letter | Status | Processed At |
| --- | ------- | ------- | -------- | ------- | -------------- | ------------ | ------ | ------------ |

---

# Workflow Logic

1. Detect new jobs from Google Sheets
2. Fetch job page HTML
3. Clean and extract text
4. Analyze with OpenAI
5. Generate structured JSON
6. Update Google Sheets
7. Send Telegram notification
8. Mark job as processed

---

# Notes

- Built for personal automation and AI workflow experimentation
- Runs locally with Docker
- No external server required
- Community Edition of n8n used

---

# Future Improvements

- LinkedIn job support
- Better HTML extraction
- Multi-agent architecture
- AI CV tailoring
- Auto-apply workflows
- Retry & error handling
- Vector search / memory
- Browser automation

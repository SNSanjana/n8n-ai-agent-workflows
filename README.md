# 🤖 AI Agent Workflows — n8n + Google Gemini

Built by **S N Sanjana** | BTech AI & ML, MSRIT Bangalore | CGPA: 9.16

Two fully autonomous AI agent workflows built using **n8n** and **Google Gemini 1.5 Flash API** — no code, pure visual automation.

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `assignment1_ceo_research_agent.json` | Autonomous internet exploration agent that researches any founder or CEO |
| `assignment2_ai_dev_assistant.json` | AI development assistant for code debugging, explanation, docs and review |

---

## 🕵️ Assignment 1 — Autonomous CEO Research Agent

### What it does
An autonomous agent that researches any founder or CEO by:
- Planning its own search queries using AI
- Browsing the internet via DuckDuckGo
- Extracting and organizing facts into memory
- Writing a full structured intelligence report

### Workflow Architecture
```
Manual Trigger → Edit Fields (Set Target + Company)
→ Basic LLM Chain (Plan Queries)
→ HTTP Request (Search Web) → Basic LLM Chain (Extract Facts)
→ Basic LLM Chain (Write Report)
```

### How to use
1. Import `assignment1_ceo_research_agent.json` into n8n
2. Add your Google Gemini API credential
3. Open the **Edit Fields** node
4. Change `target` to any founder name — example: `Sam Altman`
5. Change `company` to their company — example: `OpenAI`
6. Click **"Test Workflow"**
7. The agent automatically researches and generates a full report!

### Sample Output Structure
```
# Intelligence Profile: Sam Altman
Company: OpenAI

## 1. Executive Summary
## 2. Background & Education
## 3. Career Journey
## 4. Company Vision & Strategy
## 5. Leadership Style & Personality
## 6. Notable Achievements
## 7. Key Quotes & Philosophy
## 8. Recent News & Activity
```

---

## 🛠️ Assignment 2 — AI Development Assistant

### What it does
An AI agent that assists developers by analyzing Python code and providing:
- **debug** — finds all bugs with severity levels and fixes
- **explain** — explains what the code does in plain English
- **docs** — generates docstrings and README
- **tests** — writes complete test suite
- **review** — full code review with score
- **refactor** — cleaner improved version

### Workflow Architecture
```
Manual Trigger → Edit Fields (Paste Code + Choose Mode)
→ Basic LLM Chain (Analyze with Gemini)
```

### How to use
1. Import `assignment2_ai_dev_assistant.json` into n8n
2. Add your Google Gemini API credential
3. Open the **Edit Fields** node
4. Paste your Python code in the `code` field
5. Set the `mode` field to: `debug` / `explain` / `docs` / `tests` / `review` / `refactor`
6. Click **Test Workflow**
7. See the full analysis in the output panel!

### Demo
The workflow comes pre-loaded with a sample buggy `UserManager` class containing **7 intentional bugs** including:
- Plain text password storage (CRITICAL)
- Missing file existence check (CRITICAL)
- Division by zero error (HIGH)
- Unhandled JSON decode error (HIGH)
- Missing error handling on save (HIGH)
- KeyError on delete (MEDIUM)
- Fake timestamp (LOW)

---

## 🔧 Setup Instructions

### Prerequisites
- n8n installed (localhost or cloud)
- Google Gemini API key (get free at aistudio.google.com)

### Import Workflow
1. Open n8n
2. Click **"New Workflow"**
3. Click **⋯ menu** → **"Import from file"**
4. Upload the JSON file
5. Go to Settings → Credentials → Add Google Gemini API key
6. Save and run!

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| n8n | Visual workflow automation |
| Google Gemini 1.5 Flash | AI language model |
| DuckDuckGo | Web search (no API key needed) |
| HTTP Request node | Web browsing and scraping |

---

## 👩‍💻 About Me

I'm Sanjana, a 3rd year BTech AI & ML student at MSRIT Bangalore with a CGPA of 9.16. I love building AI automation systems and agentic workflows.

- 🔗 [LinkedIn](https://linkedin.com/in/snsanjana)
- 💻 [GitHub](https://github.com/SNSanjana)

---

*Built for Aadi Foundation AI Tutor Internship Assignment*

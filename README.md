# AI Resume Screening System — Nutrabay Assessment

An end-to-end automated resume screening system built with n8n, Groq AI, and Google Sheets. Evaluates multiple candidates against a Job Description and generates structured hiring recommendations — fully automated, zero manual effort.

---

## 🚀 How It Works

1. Job Description and candidate resumes are stored in Google Sheets
2. n8n workflow triggers and loops through each candidate
3. Each resume is sent to Groq's LLaMA 3.3 70B model via API
4. AI evaluates the candidate and returns structured JSON output
5. Results are automatically written back to the Output tab in real time

---

## 📊 Output

For each candidate the system generates:

| Field | Description |
|---|---|
| Candidate | Name |
| Score | Match score (0–100) |
| Strengths | 2–3 key strengths vs JD |
| Gaps | 2–3 missing skills or experience |
| Recommendation | Strong Fit / Moderate Fit / Not Fit |
| Summary | One-line hiring manager note |

🔗 **Live Output Sheet:** https://docs.google.com/spreadsheets/d/1RptLqIL8Xe3xfi-bZaTIvAQfbMo0U3hjZ9qmJgqeiDk/edit?gid=632036102#gid=632036102

---

## 🛠️ Tools Used

- **n8n** — workflow automation
- **Groq API** (LLaMA 3.3 70B) — AI evaluation
- **Google Sheets** — data input and output

---

## 📁 Repository Structure
```
nutrabay-resume-screener/
├── workflow.json       # n8n workflow (importable)
└── README.md
```

---

## ⚙️ How to Run

1. Import `workflow.json` into your n8n instance
2. Connect your Google Sheets and Groq API credentials
3. Add your JD and resumes to the sheet
4. Click Execute Workflow
5. View results in the Output tab instantly

---

## 💡 Key Features

- Fully automated — no manual scoring
- Reusable for any role — just swap the JD
- Structured, consistent output every time
- Runs 7 candidates in under 2 minutes

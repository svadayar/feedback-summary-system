# feedback-summary-system
# AI-Powered Client Feedback Summarization System

This project is an end-to-end pipeline that ingests multi-channel client feedback
(emails, documents, chat messages), stores it in AWS S3 and Snowflake, processes it 
using LLMs (GPT-4, Claude, or Mistral), and provides summarized feedback per client via an API and dashboard for business teams.

---

## 📌 Features
- Ingest feedback from Gmail, Slack, SharePoint, and PDF/DOCX files.
- Upload raw data to AWS S3 (Raw Zone).
- Transform and load cleaned data into Snowflake via AWS Glue.
- Summarize per-client feedback using an OpenAI LLM via FastAPI.
- Display summarized feedback through a Streamlit dashboard.

---

## 📂 Folder Structure
```
ai-feedback-summary-system/
├── README.md
├── requirements.txt
├── .env.example
├── ingest/              # Scripts to ingest email, docs, chat
├── s3_upload/           # Scripts to upload to S3
├── glue_jobs/           # AWS Glue Spark job to Snowflake
├── fastapi_server/      # API to serve LLM-based summaries
├── dashboard/           # Streamlit UI
└── utils/               # Shared preprocessing utilities

AI-Powered Lead Capture & Conversion System

> Built with n8n | Zero code required to deploy | Reusable for any client

---

## What This Is

EasyStream is a fully automated lead capture and conversion system that:

- Responds to business enquiries **within 90 seconds** — 24 hours a day, 7 days a week
- Uses **Claude AI** to read, classify, and write personalised responses
- Creates CRM contacts, logs to spreadsheets, and briefs the business owner automatically
- Follows up at Day 2 and Day 7 if the lead goes quiet
- Runs entirely on **n8n** — self-hosted, no per-operation fees

Built for: care homes, dental clinics, recruitment agencies, healthcare providers, and any business that relies on enquiries.

---

## The Problem It Solves

| Problem | Impact |
|---|---|
| Average UK care home response time: 47 hours | Families choose the first home that replies |
| 38% of enquiries arrive outside office hours | No staff = no response = lost lead |
| No follow-up system for cold leads | Revenue sitting in a spreadsheet going nowhere |
| Manual CV screening: 23 hours per hire | Recruiters spending billable time on admin |

---

## Flow 1 — AI Enquiry Interceptor

**Trigger:** Form submission (Tally.so)
**Response time:** Under 90 seconds
**Runs:** 24/7, fully automated

```
Form Submitted (Tally.so)
        ↓
Parse & Extract Fields (Code Node)
        ↓
AI Classification — Claude Haiku
  → Urgency: URGENT / ROUTINE / INFO_ONLY
  → Sentiment: DISTRESSED / CALM / ENQUIRING
        ↓
AI Message Writing — Claude Sonnet
  → Personalised response in business voice
  → Tone adjusts based on urgency
        ↓
Email sent to enquirer (Gmail)
        ↓
Owner briefed with full summary (Gmail)
        ↓
Contact created in HubSpot CRM
        ↓
Row logged in Google Sheets
        ↓
Wait 24 hours
        ↓
Day 2 AI follow-up (Claude Haiku)
        ↓
Wait 6 more days
        ↓
Day 7 final follow-up (Claude Sonnet)
        ↓
Lead marked cold in HubSpot
```

**Nodes used:** Webhook, Code (x4), HTTP Request (x3 — Anthropic API), Gmail (x3), HubSpot, Google Sheets, Wait (x2)

---

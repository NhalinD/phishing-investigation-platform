# Phishing Investigation Platform — API Contract

Version: 1.0

This document is the single source of truth for communication
between the frontend and backend.

Do NOT independently rename endpoints, fields, or response structures.

---

# 1. Analyze Phishing Message

## Endpoint

POST /api/analyze

## Purpose

Analyze a suspicious email/message and return:
- Overall risk score
- Verdict
- Confidence
- Triggered indicators
- Evidence
- Recommended action
- Analysis summary

---

## Request

Content-Type: application/json

```json
{
  "sender": "security@paypa1-login.com",
  "subject": "Your account will be suspended!",
  "body": "Your account will be suspended. Verify immediately.",
  "url": "http://paypa1-login.com/verify",
  "attachments": []
}
# 🤖 AI Lead Management Automation

An AI-powered lead qualification and automated follow-up system built with **n8n, OpenAI, Google Sheets, and Gmail**.

This workflow automatically receives lead information, analyzes and scores the lead using AI, classifies the lead as HOT, WARM, or COLD, stores the lead in a Google Sheets CRM, and sends a personalized follow-up email.

---

## 🚀 Project Overview

Manual lead qualification can take time and important leads may be missed.

This automation solves that problem by automatically:

1. Receiving lead data through a webhook
2. Analyzing the lead using OpenAI
3. Calculating a lead score from 0–100
4. Classifying the lead as HOT, WARM, or COLD
5. Assigning a priority
6. Saving the lead into Google Sheets
7. Routing the lead based on temperature
8. Sending a personalized Gmail follow-up
9. Updating the CRM email status

---

## 🏗️ Workflow Architecture

```text
Lead / API Request
       ↓
    Webhook
       ↓
   OpenAI Analysis
       ↓
 JavaScript Scoring
       ↓
 Google Sheets CRM
       ↓
      Switch
   ↙     ↓      ↘
 HOT   WARM    COLD
  ↓      ↓       ↓
Gmail  Gmail   Gmail
  ↓      ↓       ↓
Update Update  Update
Sheet  Sheet   Sheet

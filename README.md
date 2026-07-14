# 🤖 AI Lead Qualification Agent

An AI-powered Lead Qualification Agent built with **n8n** and **Google Gemini** that automatically analyzes incoming business leads, scores them based on multiple business factors, stores them in Google Sheets, and notifies the sales team about high-priority opportunities.

---

## 🚀 Features

- 📥 Accepts business leads through a Webhook
- 🤖 AI-powered lead analysis using Google Gemini
- 📊 Generates a Lead Score (0–100)
- 🚦 Classifies leads as High, Medium, or Low priority
- 💼 Recommends the most suitable AI service
- 📝 Provides reasoning behind the lead score
- 📌 Suggests the next sales action
- 💰 Estimates project value
- 📄 Generates a concise business summary
- 📈 Automatically stores all leads in Google Sheets
- 📧 Sends Gmail notifications for high-priority leads
- 🔀 Uses conditional workflow with IF Node
- 🌐 Returns a structured JSON API response

---

## 🛠️ Tech Stack

- n8n
- Google Gemini
- Google Sheets
- Gmail
- Webhooks
- Structured Output Parser
- IF Node
- Postman

---

## 🏗️ Workflow Architecture

```text
POST Request
      │
      ▼
Webhook
      │
      ▼
Google Gemini AI
      │
      ▼
Structured Output Parser
      │
      ▼
IF Node
 ├──────────────┐
 ▼              ▼
High        Medium/Low
 │              │
 ▼              ▼
Google Sheets  Google Sheets
 │
 ▼
Gmail Notification
 │
 ▼
Respond to Webhook
```

---

## 📥 Sample Input

```json
{
  "name": "Sarah Johnson",
  "email": "sarah@startup.com",
  "company": "StartupX",
  "industry": "Education",
  "budget": 10000,
  "employees": 30,
  "requirement": "Need AI automation for email support and lead management.",
  "timeline": "1 month"
}
```

---

## 📤 Sample API Response

```json
{
  "success": true,
  "message": "Lead processed successfully.",
  "leadScore": 80,
  "priority": "High",
  "recommendedService": "AI Automation Services",
  "nextAction": "Follow up with a demo"
}
```

---

## 📊 Sample AI Output

```json
{
  "leadScore": 80,
  "priority": "High",
  "recommendedService": "AI Automation Services",
  "reason": "The company has a clear business requirement and sufficient budget.",
  "nextAction": "Schedule a discovery call within 24 hours.",
  "estimatedProjectValue": "$10,000",
  "summary": "StartupX requires AI automation for email support with a one-month implementation timeline."
}
```

---

## 📈 Lead Evaluation Criteria

The AI evaluates each lead based on:

- Budget
- Company Size
- Industry
- Requirement Clarity
- Timeline
- Business Need
- Potential Project Value

---

## 📧 High Priority Workflow

When a lead receives a **High Priority** score:

- ✅ Store lead in Google Sheets
- ✅ Send Gmail notification
- ✅ Return success response to the client

For **Medium** and **Low Priority** leads:

- ✅ Store lead in Google Sheets
- ❌ No Gmail notification
- ✅ Return success response

---

## 🌐 API Response

The workflow returns a clean JSON response suitable for frontend applications.

Example:

```json
{
  "success": true,
  "message": "Lead processed successfully.",
  "leadScore": 80,
  "priority": "High",
  "recommendedService": "AI Automation Services",
  "nextAction": "Follow up with a demo"
}
```

---

## 🎯 Use Cases

- AI Lead Qualification
- Sales Automation
- CRM Automation
- Marketing Lead Scoring
- Business Process Automation
- AI Sales Assistant
- Customer Lead Prioritization

---

## 📂 Project Structure

```
ai_lead_qualification_agent/
│
├── ai_lead_qualification_agent.json
├── README.md
└── Screenshots/
```

---

## ⚙️ How to Test

### Using Postman

1. Create a **POST** request.
2. Paste the n8n Webhook URL.
3. Set the header:

```
Content-Type: application/json
```

4. Send a business lead as JSON.
5. Observe the AI-generated response.
6. Verify:
   - Google Sheets updated.
   - Gmail notification (High Priority only).
   - JSON response returned.

---

## 📸 Screenshots

### n8n Workflow

<img width="1673" height="801" alt="Screenshot 2026-07-14 175332" src="https://github.com/user-attachments/assets/05720eb5-870c-4b4e-bc38-f3e8e00285fc" />


### Google Sheets

<img width="1896" height="300" alt="Screenshot 2026-07-14 175826" src="https://github.com/user-attachments/assets/bf77ac6b-c82b-4e0f-954e-9ebd7f0740e2" />


### Gmail Notification

<img width="1917" height="915" alt="Screenshot 2026-07-14 180109" src="https://github.com/user-attachments/assets/49308f9c-c2da-4c3f-b192-ba02cf28e213" />


### Postman Request

<img width="796" height="661" alt="Screenshot 2026-07-14 180156" src="https://github.com/user-attachments/assets/d6cfda7a-9657-4905-90b4-d9786eea0120" />


### API Response

<img width="810" height="337" alt="Screenshot 2026-07-14 180225" src="https://github.com/user-attachments/assets/29f61418-971e-4ee0-bd89-882fcc98846d" />


---

## ✨ Version 2 Enhancements

- Google Sheets Integration
- Gmail Notifications
- Conditional Workflow using IF Node
- AI Lead Qualification
- Automated Lead Storage
- Structured API Response
- Business Workflow Automation

---

## 🔮 Future Improvements

- HubSpot Integration
- Salesforce Integration
- Slack Notifications
- Microsoft Teams Notifications
- Lead Analytics Dashboard
- PDF Lead Reports
- Multi-language Support
- Follow-up Email Automation

---

## 👨‍💻 Author

**Chaitanya Ramisetti**

AI Engineering | AI Automation | Python Developer

GitHub: https://github.com/chaitanyaramisetti4589-gif

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub!

Feedback and contributions are always welcome.

# 🤖 AI Lead Qualification Agent

An AI-powered Lead Qualification Agent built with **n8n** and **Google Gemini** that automatically analyzes incoming business leads, scores them based on multiple factors, and returns structured insights to help sales teams prioritize prospects.

---

## 🚀 Features

- 📥 Accepts lead information via Webhook
- 🧠 Uses Google Gemini AI to analyze lead quality
- 📊 Generates a Lead Score (0–100)
- 🚦 Assigns Priority (High, Medium, Low)
- 💼 Recommends the most suitable AI service
- 📝 Explains the reasoning behind the score
- ✅ Suggests the next action for the sales team
- 💰 Estimates project value
- 📄 Returns structured JSON output

---

## 🛠️ Tech Stack

- **n8n**
- **Google Gemini**
- **Webhook**
- **Structured Output Parser**
- **Postman** (for testing)

---

## 📌 Workflow

```
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
  "requirement": "Need AI automation for emails.",
  "timeline": "1 month"
}
```

---

## 📤 Sample Output

```json
{
  "leadScore": 80,
  "priority": "High",
  "recommendedService": "AI Email Automation",
  "reason": "The company has a clear requirement and a budget in place.",
  "nextAction": "Schedule a discovery call within 24 hours.",
  "estimatedProjectValue": "$10,000",
  "summary": "StartupX needs AI automation for emails with a budget of $10,000 and a timeline of 1 month."
}
```

---

## 📊 Lead Evaluation Criteria

The AI evaluates each lead using:

- Budget
- Company Size
- Industry
- Requirement Clarity
- Timeline
- Business Need

---

## 🎯 Use Cases

- Sales Lead Qualification
- CRM Automation
- Marketing Lead Scoring
- AI Sales Assistant
- Business Process Automation

---

## 📁 Project Structure

```
ai-lead-qualification-agent/
│
├── workflow.json
├── README.md
└── screenshots/
```

---

## 🧪 How to Test

### Using Postman

1. Create a **POST** request.
2. Paste the Webhook URL from n8n.
3. Set:

```
Content-Type: application/json
```

4. Send a JSON payload.
5. Receive the AI-generated lead analysis.

---

## 📈 Future Improvements

- Google Sheets Integration
- Gmail Notifications
- Slack Alerts
- CRM Integration (HubSpot/Salesforce)
- Lead Dashboard
- Analytics & Reporting
- Multi-language Support

---

## 📸 Screenshots

### n8n Workflow

<img width="1667" height="793" alt="workflow" src="https://github.com/user-attachments/assets/6c1f0702-1e1c-4797-af8b-46df70fd6b3a" />


### Postman Request

<img width="815" height="605" alt="request" src="https://github.com/user-attachments/assets/74032ba8-e2ef-4b37-80f2-fc6878fcce98" />


### AI Response

<img width="802" height="582" alt="response" src="https://github.com/user-attachments/assets/cddd2e41-364a-44dd-9fe8-0376cb39ba19" />


---

## 👨‍💻 Author

**Chaitanya Ramisetti**

AI Engineering & AI Automation Enthusiast

GitHub: https://github.com/chaitanyaramisetti4589-gif

---

## ⭐ If you found this project useful, consider giving it a star!

# AI Appointment Booking Assistant

An AI-powered appointment booking workflow built with **n8n**, **Gemini AI**, **Google Calendar**, **Gmail**, and **JavaScript**.

The workflow automatically extracts booking details from natural language, checks Google Calendar availability, creates appointments, and sends confirmation emails.

---

# Business Problem

Many businesses manually process appointment requests from emails, websites, or contact forms.

This often causes:

- Double bookings
- Slow response times
- Manual scheduling
- Human errors
- Increased administrative work

This workflow automates the entire booking process.

---

# Solution

The workflow performs the following steps:

1. Receives a booking request via Webhook.
2. Uses Gemini AI to extract appointment details.
3. Converts AI output into structured JSON.
4. Checks Google Calendar availability.
5. Creates a calendar event if the slot is available.
6. Sends a confirmation email.
7. Sends an unavailable notification if the slot is already booked.

---

# Features

- AI-powered appointment extraction
- Natural language processing
- Google Calendar integration
- Gmail integration
- Automatic availability check
- Automatic event creation
- Confirmation emails
- Busy notifications
- Conditional workflow logic
- Error handling

---

# Tech Stack

- n8n
- Gemini AI API
- Google Calendar API
- Gmail API
- JavaScript
- Webhooks

---

# Workflow Overview

```text
Webhook
      │
      ▼
Gemini AI
      │
      ▼
JavaScript Parser
      │
      ▼
Google Calendar
(Check Availability)
      │
      ▼
IF
 ┌──────────────┐
 │              │
 ▼              ▼
Available     Busy
 │              │
 ▼              ▼
Create Event  Send Busy Email
 │
 ▼
Send Confirmation Email
 │
 ▼
Respond to Webhook
```

---

# Project Structure

```text
.
├── workflow.json
├── README.md
└── images
    ├── workflow.png
    ├── booking-request.png
    ├── calendar-event.png
    └── confirmation-email.png
```

---

# Screenshots

| Workflow | Booking Request |
|-----------|-----------------|
| <img src="./images/workflow2.png.png" width="100%"> | <img src="./images/requiest1.png.png" width="100%"> |

| Calendar Event | Confirmation Email |
|----------------|--------------------|
| <img src="./images/calendar.png.png" width="100%"> | <img src="./images/confirmation-email.png" width="100%"> |

---

# Example Request

```text
Hello,

My name is John Smith.

I'd like to book a meeting tomorrow at 2 PM.

My email is john@example.com.
```

---

# AI Output

```json
{
  "name": "John Smith",
  "email": "john@example.com",
  "date": "2026-07-18",
  "time": "14:00"
}
```

---

# Business Benefits

- Faster customer response
- Reduced manual work
- No double bookings
- Automated scheduling
- Better customer experience
- Easy to customize
- Production-ready foundation

---

# Challenges Solved

During development several real-world automation challenges were addressed:

- AI response normalization
- 24-hour time formatting
- Google Calendar availability detection
- Data persistence between workflow nodes
- Conditional workflow routing
- API response parsing
- Dynamic email generation

---

# Possible Improvements

- Outlook Calendar integration
- Microsoft Teams integration
- Automatic free-slot suggestions
- Time zone detection
- CRM integration
- Slack notifications
- SMS reminders
- Appointment cancellation
- Appointment rescheduling
- Database logging
- Multi-user scheduling

---

# Skills Demonstrated

- AI Automation
- Workflow Design
- API Integration
- Prompt Engineering
- JavaScript
- Data Transformation
- Business Process Automation
- Google Workspace Automation
- Error Handling
- Production Workflow Development

---

# Repository Contents

- Workflow JSON
- Project documentation
- Architecture overview
- Workflow screenshots
- Example input/output

---

# Author

Built by **Zvc Qds** as part of an AI Automation Engineering portfolio..

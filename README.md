# AI Appointment Booking Assistant

An AI-powered appointment booking workflow built with **n8n**, **Gemini AI**, **Google Calendar**, **Gmail**, and **JavaScript**.

The workflow automatically extracts booking details from a natural language request, checks calendar availability, creates a Google Calendar event if the requested slot is free, and sends a confirmation email. If the requested time is unavailable, the customer receives a notification asking them to choose another time.

---

# Business Problem

Many small businesses manually manage appointment requests received through websites, emails, or contact forms.

This process often leads to:

- Double bookings
- Slow response times
- Manual calendar management
- Missed appointments
- Increased administrative work

This workflow automates the entire booking process.

---

# Solution

The automation performs the following steps:

1. Receives an appointment request.
2. Uses Gemini AI to extract booking information.
3. Converts the AI response into structured JSON.
4. Checks Google Calendar for existing events.
5. Creates a calendar event if the time slot is available.
6. Sends a confirmation email.
7. Sends an unavailable notification if the slot is already booked.

---

# Features

- AI-powered information extraction
- Natural language appointment requests
- Google Calendar integration
- Gmail integration
- Automatic availability check
- Automatic appointment creation
- Email notifications
- Conditional workflow logic
- Error handling
- JSON parsing

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
Webhook Response
```

---

# Project Structure

```
/
├── workflow.json
├── README.md
└── images/
    ├── workflow.png
    ├── booking-request.png
    ├── calendar-event.png
    ├── confirmation-email.png
```

---

# Screenshots

## Workflow

![Workflow](images/workflow2.png)

---

## Booking Request

![Request](images/request1.png)

---

## Calendar Event

![Calendar](images/calendar.png)
---


## Confirmation Email

![Email](images/confirmation-email.png)

---

# Example Request

```
Hello,

My name is John Smith.

I'd like to schedule a meeting tomorrow at 2 PM.

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
- Fully automated scheduling
- Improved customer experience
- Easy to customize
- Ready for production improvements

---

# Challenges Solved

During development several real-world integration issues were solved:

- AI output normalization
- 24-hour time formatting
- Google Calendar availability detection
- Data persistence between workflow nodes
- Conditional routing
- API response parsing
- Dynamic email generation

---

# Possible Improvements

- Multiple calendars
- Outlook Calendar support
- Automatic free-slot suggestions
- Time zone detection
- CRM integration
- Slack notifications
- SMS reminders
- Rescheduling
- Cancellation workflow
- Database logging

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
- Production Workflow Design

---

# Author

Built by **Zvc Qds** as part of an AI Automation Engineering portfolio.

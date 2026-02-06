---
description: Create quotes using natural language conversation.
---

# 🤖 AI Assistant (Beta)

{% hint style="warning" %}
**Beta Feature** — The AI Assistant is currently in beta testing. Features may change, and occasional unexpected behavior may occur. We'd love your feedback!
{% endhint %}

The AI Assistant lets you create quotes by simply describing what you need in plain English. No forms to fill out — just tell it what you want.

---

## Getting Started

### Opening the AI Assistant

1. From the **Dashboard**, find the **AI Assistant (Beta)** card
2. Click **Open Chat**
3. A chat window opens on the right side of your screen

### Your First Conversation

The AI Assistant greets you with example prompts to get started. Try something like:

> "Quote from KLAX to KSEA on February 15 at 9am"

The Assistant will:
1. Parse the airports, date, and time
2. Check which aircraft in your fleet can make the trip
3. Generate a quote estimate
4. Ask if you'd like to proceed

---

## What You Can Ask

### Quote Creation

The most common use case — describe a flight and get a quote:

| Example Prompt | What it does |
|----------------|--------------|
| "Quote from KLAX to KSEA on March 1 at 10am" | Creates a one-way quote |
| "Round trip Sydney to Melbourne tomorrow" | Creates a return flight quote |
| "Quote JFK to MIA for 4 passengers" | Includes passenger count |
| "Multi-leg: LAX → SFO → SEA next Monday" | Creates multi-stop itinerary |

### Fleet Questions

Ask about your aircraft capabilities:

| Example Prompt | What it does |
|----------------|--------------|
| "What aircraft can fly more than 2000nm?" | Lists capable aircraft |
| "Which aircraft is available on Friday?" | Checks fleet availability |
| "Show me aircraft that seat 6 or more" | Filters by capacity |

### Quick Information

Get fast answers about your operation:

| Example Prompt | What it does |
|----------------|--------------|
| "How far is it from Sydney to Brisbane?" | Distance calculation |
| "What's the flight time LAX to Vegas?" | Time estimate |

---

## Creating a Quote Step-by-Step

### 1. Describe the Flight

Type a natural description:

> "I need a quote from Brisbane to Sydney on February 20th at 2pm for 3 passengers"

### 2. Review the Estimate

The AI will respond with:
- Identified airports
- Date and time
- Suggested aircraft options
- Estimated costs

### 3. Select Aircraft

If multiple aircraft can make the trip, you'll see options. Tell the AI which ones to include:

> "Use the King Air and the Citation"

Or:

> "Just the King Air"

### 4. Confirm Creation

Once you're happy, the AI will ask for confirmation before creating the quote. Reply:

> "Yes, create the quote"

### 5. Quote Created

The AI provides a link to your new quote. Click to open it in the full quote editor.

---

## Tips for Better Results

{% hint style="success" %}
**Be specific with dates and times** — "Next Tuesday at 3pm" works better than "sometime next week"
{% endhint %}

### Airport Codes vs. City Names

Both work, but airport codes are more precise:

- ✅ "YBBN to YSSY" — unambiguous
- ✅ "Brisbane to Sydney" — works, AI will ask if multiple airports
- ⚠️ "New York to LA" — may need clarification (JFK? LGA? EWR?)

### Handling Ambiguity

If the AI isn't sure which airport you mean, it will ask. Just clarify:

> AI: "Did you mean KJFK or KLGA for New York?"
> You: "JFK"

### Date Formats

The AI understands various formats:

- "February 15" or "Feb 15" or "15 Feb"
- "Next Monday" or "this Friday"
- "Tomorrow at 9am"
- "In 2 weeks"

---

## Contacts

When creating a quote, the AI may ask about the customer. You can:

- Provide a name: "It's for John Smith"
- Search contacts: "Look up Acme Corp"
- Skip for now: "I'll add the contact later"

If the contact doesn't exist, the AI can create one for you.

---

## Limitations (Beta)

While in beta, the AI Assistant has some limitations:

- **Complex pricing adjustments** — For detailed cost editing, use the full quote editor
- **Document attachments** — Add documents through the quote page after creation
- **Historical lookups** — "Show me last month's quotes" isn't supported yet
- **Booking creation** — Currently quotes only; convert to bookings through the quote page

---

## Feedback

We're actively improving the AI Assistant. If you encounter issues or have suggestions:

- Note what you asked and what went wrong
- Contact support with your feedback
- Your input helps us make it better!

{% hint style="info" %}
**📹 Video Coming Soon**

**Runsheet for Tom:**
1. Open Dashboard, click "Open Chat" on AI Assistant card
2. Show the welcome message with example prompts
3. Type: "Quote from Brisbane to Sydney on February 20 at 2pm"
4. Show the AI parsing and suggesting aircraft
5. Select an aircraft option
6. Confirm quote creation
7. Click the link to show the created quote
8. **Duration:** ~2-3 minutes
{% endhint %}

---

## Next Steps

- [Dashboard Overview](README.md) — Back to Dashboard features
- [Quote Details](../quotes/README.md) — Working with quotes after creation
- [Aircraft Management](../aircraft/README.md) — Configure your fleet for better AI suggestions

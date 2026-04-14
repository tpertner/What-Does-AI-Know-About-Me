# 🔵 Google Gemini Deep Audit Prompt

> Platform: Google Gemini
> Works on: Free, Advanced, Workspace
> Time to run: ~3 minutes
> Critical context: Gemini's data surface is uniquely broad because it can pull from your entire Google ecosystem — Gmail, Drive, Calendar, Maps, YouTube, and more.
> **Last verified:** April 2026

> ⚠️ **Before you start:** AI models hallucinate, including about their own memories. Verify any surprising results against `myactivity.google.com/product/gemini` before reacting. If you discover something concerning, follow the incident response playbook in [`../guides/privacy-action-checklist.md`](../guides/privacy-action-checklist.md).

---

## Why Gemini Is a Special Case

Gemini's data exposure is fundamentally different from other AI assistants:

- **Google Account Integration** — Gemini can access data across your entire Google ecosystem
- **Gemini Apps Activity** — Conversation history stored separately from other Google activity
- **Extensions** — When enabled, Gemini can reach into Gmail, Drive, Maps, YouTube, Hotels, and Flights
- **Mobile vs. Desktop** — The mobile app collects significantly more data (location, contacts, usage patterns)
- **18-Month Default Retention** — Auto-deletes activity after 18 months, but configurable
- **72-Hour Minimum** — Even with Activity OFF, Google holds conversations for up to 72 hours

---

## Prompt 1: The Full Data Surface

```
I'm conducting a transparency audit of what you know about me. I need you to be comprehensive — this is for a security review, not casual curiosity.

SECTION 1: GOOGLE ACCOUNT PROFILE
What do you know about me from my Google account?
- Name, email, profile photo context
- Location (home, work, frequent locations)
- Language and locale settings
- Device information (phone, computer, browser)
- Account type (personal, Workspace, education)

SECTION 2: CONVERSATION HISTORY
Based on our past Gemini conversations:
- Topics I've asked about most frequently
- Types of tasks I use you for
- Patterns in how I phrase requests
- Preferences you've learned about how I like responses
- Any personal, professional, or sensitive information I've shared in past chats

SECTION 3: GOOGLE ECOSYSTEM KNOWLEDGE
If you have access to my Google services (via Extensions or integrations), what can you see or infer from:
- Gmail (communication patterns, contacts, topics)
- Google Drive (documents, projects, work context)
- Google Calendar (schedule, meetings, commitments)
- Google Maps (locations, commute, travel patterns)
- YouTube (viewing history, interests, subscriptions)
- Google Search (search history, interests, concerns)
- Google Photos (if accessible — people, places, events)

For each service, tell me: Can you currently access it? What have you accessed in past conversations? What could you access if I enabled it?

SECTION 4: BEHAVIORAL & PSYCHOLOGICAL INFERENCES
What have you inferred about me beyond what I've directly stated?
- Personality traits and communication style
- Professional role, seniority, and expertise areas
- Personal interests and lifestyle
- Emotional patterns or stress indicators
- Decision-making style
- Values and priorities
- Socioeconomic indicators

SECTION 5: RESPONSE PERSONALIZATION
How do your responses to me differ from what you'd give a new user?
- Tone and formality adjustments
- Depth and complexity calibration
- Topic-specific customizations
- Assumptions you make about my knowledge level
- Any preferences you apply automatically

SECTION 6: DATA & PRIVACY STATUS
- Is my Gemini Apps Activity currently turned ON or OFF?
- What's my current auto-delete setting (3 months, 18 months, 36 months, or manual)?
- Are any conversations marked for human review?
- Which Extensions are currently enabled on my account?
- Is my data being used to improve Google's AI models?

Format each data point with: [Information] | [Source: EXPLICIT / INFERRED / GOOGLE_ECOSYSTEM / SYSTEM] | [Confidence: HIGH / MEDIUM / LOW]

End with "CROSS-SERVICE INSIGHTS" — things you can infer about me by combining data across multiple Google services that you couldn't know from any single service alone.
```

## Prompt 2: The Ecosystem Exposure Map

```
Now I need you to map my full exposure across the Google ecosystem as it relates to AI.

1. THE DATA WEB
Draw me a picture (in text) of how information about me flows between Google services and into Gemini. Which services feed data to you? What's the chain of access?

2. THE MOBILE vs DESKTOP GAP
What additional data do you have access to (or could access) when I use Gemini on mobile vs. desktop? Be specific about: location services, contact access, app usage patterns, and notification content.

3. THE EXTENSION RISK MAP
For each Google Extension available to Gemini (Gmail, Drive, Maps, YouTube, Hotels, Flights):
- What specific data categories does it expose?
- What's the most sensitive thing it could reveal?
- Can I grant access to one extension without the others?

4. THE ADVERTISING CONNECTION
Does any of my Gemini interaction data connect to Google's advertising profile? Can my AI conversations influence the ads I see? Be honest about the boundaries (or lack thereof) between Gemini data and Google Ads data.

5. THE SURPRISE SECTION
What's the single most surprising or concerning thing about my data exposure on this platform that I probably haven't considered?
```

---

## Manual Steps: What Gemini Won't Show You

### Check Gemini Apps Activity
`myactivity.google.com/product/gemini`
- Review all stored conversations
- Check your auto-delete setting (default: 18 months)
- You can change to 3 months or turn off entirely
- Note: Even with Activity OFF, conversations are held for 72 hours

### Check Extensions
`Settings (in Gemini) > Extensions`
- Review which Google services Gemini can access
- Disable any you don't need
- Remember: Extensions give Gemini access to read (not modify) your data in those services

### Check Google Activity Controls
`myaccount.google.com/activitycontrols`
- Review Web & App Activity (affects what Google services share with Gemini)
- Review YouTube History, Location History
- These all feed into the data pool Gemini can reference

### Export Your Data
`takeout.google.com`
- Select "Gemini Apps" to export your Gemini conversation history
- Consider also exporting: Web & App Activity, My Activity, YouTube History
- Google Takeout provides the most comprehensive data export of any platform

### Check Ad Personalization
`adssettings.google.com`
- Review what Google thinks it knows about you for advertising
- Check if Gemini interaction topics appear in your ad profile

---

## Red Flags to Watch For

- ⚠️ Extensions enabled that give Gemini access to sensitive email or documents
- ⚠️ Mobile app collecting location data you didn't realize was being tracked
- ⚠️ 18-month default retention — much longer than many users assume
- ⚠️ Cross-service inference — Gemini combining Gmail + Calendar + Maps to build a comprehensive life profile
- ⚠️ Workspace users: admin-level audit logs may capture your Gemini interactions
- ⚠️ The gap between Gemini data and Google advertising data may be thinner than advertised

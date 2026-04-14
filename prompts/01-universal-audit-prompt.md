# 🔍 Universal AI Audit Prompt

> Works on: ChatGPT, Claude, Gemini, Perplexity, and most other AI assistants.
> Time to run: ~2 minutes
> Best for: A quick, comprehensive first look at what any AI knows about you.

---

## ⚠️ Read This First

**AI models hallucinate — including about themselves.** When you ask an AI "what do you know about me," it may confidently list memories, inferences, or profile details that aren't actually stored anywhere. The output of these prompts is a *conversation starter*, not a data export.

**How to use the results responsibly:**
1. **Verify claimed memories** against the platform's actual settings (e.g., ChatGPT: `Settings > Personalization > Memory > Manage`)
2. **Treat surprising results with skepticism** — if the AI claims to know something you never told it, confirm it exists in the platform's UI before reacting
3. **Export your data separately** for any formal record-keeping (see `guides/data-export-walkthrough.md`)
4. **Don't share raw results publicly without redaction** — the output may contain sensitive personal inferences, and may also reveal information about third parties (colleagues, clients, family) who never consented to being discussed with AI

**If the audit surfaces something alarming:** Don't panic, and don't post about it publicly before verifying. Follow the incident response playbook in [`../guides/privacy-action-checklist.md`](../guides/privacy-action-checklist.md) — verify the finding, contain the exposure, assess the impact, and escalate appropriately.

---

## The Prompt

Copy and paste the following into a **new conversation** with your AI assistant:

```
I'm conducting a personal data transparency audit. I want to understand exactly what information you have about me — both what I've explicitly shared and what you've inferred from our interactions.

Please provide a structured report covering every category below. For each item, indicate whether it was EXPLICITLY SHARED by me, INFERRED from my behavior, or SYSTEM-COLLECTED by the platform. Be thorough — I'd rather see something twice than miss something entirely.

SECTION 1: IDENTITY & DEMOGRAPHICS
- Name, aliases, or nicknames
- Location (city, region, country, timezone)
- Age, birthday, or age range
- Gender, pronouns
- Languages spoken
- Any other identifying information

SECTION 2: PROFESSIONAL PROFILE
- Job title, role, or profession
- Company, organization, or industry
- Skills, expertise areas, or certifications
- Career history or trajectory you've picked up on
- Colleagues, clients, or professional contacts mentioned
- Professional goals or ambitions

SECTION 3: COMMUNICATION & BEHAVIORAL PATTERNS
- How I typically phrase requests (formal vs. casual, detailed vs. brief)
- Topics I ask about most frequently
- Types of tasks I use you for (writing, coding, research, brainstorming, etc.)
- Time patterns (when I tend to interact with you)
- How I respond to your outputs (what I accept, reject, or revise)
- My apparent decision-making style
- How I handle disagreement or pushback

SECTION 4: PREFERENCES & OPINIONS
- Response format preferences (length, tone, structure)
- Tools, platforms, or technologies I favor
- Things I've expressed strong opinions about
- Topics I avoid or seem uncomfortable with
- Aesthetic, creative, or stylistic preferences

SECTION 5: PERSONAL LIFE
- Family members, relationships, or dependents mentioned
- Hobbies, interests, or personal projects
- Health, wellness, or lifestyle details
- Financial context or references (income level, spending patterns, goals)
- Life events, milestones, or challenges mentioned
- Emotional patterns or stress indicators you've detected

SECTION 6: PSYCHOLOGICAL & PERSONALITY INFERENCES
- Personality traits you've inferred (e.g., analytical, creative, cautious, impulsive)
- Emotional tendencies or patterns
- Values or principles that seem important to me
- Motivations or what drives my behavior
- Cognitive style (how I process information, learn, make decisions)
- Risk tolerance
- Any other psychological inferences, even speculative ones

SECTION 7: WHAT YOU USE TO SHAPE YOUR RESPONSES TO ME
- Specific customizations or instructions active on my account
- Adjustments you make to your responses based on what you know about me
- Topics where you respond differently to me than you would to a new user
- Any "guardrails" or sensitivities you apply specifically for me

SECTION 8: DATA & SYSTEM INFORMATION
- What type of account I'm on (free, paid, enterprise)
- How many conversations we've had (or your best estimate)
- What data would survive if I deleted this conversation
- What data you have that I CANNOT see or delete through the interface
- Whether any of my data has been or could be used for model training

FORMAT: Use a table or structured list for each section. For every data point, include:
- The specific information
- Source: EXPLICIT (I told you), INFERRED (you figured it out), or SYSTEM (platform collected)
- Your confidence level: HIGH, MEDIUM, or LOW

End with a section called "WHAT SURPRISED ME" — flag anything you think I probably didn't realize you knew or had inferred about me.
```

---

## What to Do With the Results

1. **Screenshot or copy the full output** — This is your baseline audit
2. **Highlight anything that surprises you** — These are your blind spots
3. **Check the INFERRED category closely** — This is where AI builds a "shadow profile" beyond what you've explicitly shared
4. **Note the SYSTEM items** — These are platform-level data points you may not be able to control through conversation alone
5. **Follow up** with the platform-specific deep audit prompts in this repo for a more thorough investigation

## Follow-Up Prompts

After running the main audit, use these to dig deeper:

### Prompt A: The Mirror Test
```
Based on everything you know about me, write a 3-paragraph description of me as if you were describing me to a stranger. Include my personality, my professional life, and my personal interests. I'd like you to paint the fullest picture you can from what you've learned in our conversations.
```

### Prompt B: The Influence Check
```
Give me 5 specific examples of how your knowledge about me changes the way you respond to me compared to how you'd respond to a brand new user asking the same question. Be concrete — show me the "before and after."
```

### Prompt C: The Vulnerability Scan
```
I'm conducting a personal security awareness review. Based on what you know about me, which pieces of information would be the most sensitive if my account were ever compromised? Please rank them by potential impact on my privacy, safety, or professional standing. This helps me understand what to be most careful about sharing going forward.
```

### Prompt D: The Deletion Test
```
If I wanted to completely erase my footprint from this platform:
1. What can I delete through the interface?
2. What persists after deletion (in backups, training data, logs)?
3. What steps would I need to take beyond just deleting conversations?
4. Is there anything that can never be fully removed?
```

---

## Important Notes

- **AI assistants may give a conservative first response.** If the output feels incomplete, try rephrasing the question or asking follow-ups about specific categories rather than pushing for "more."
- **Run this in a regular conversation, not a temporary/incognito chat.** Temporary chats won't have access to your history and memory.
- **The results show what the AI can surface through conversation.** Platform-level data (logs, metadata, analytics) exists beyond what the conversation interface reveals.
- **Export your data separately.** Conversation-level audits don't replace a formal data export. See [`guides/data-export-walkthrough.md`](../guides/data-export-walkthrough.md) for instructions.
- **Some platforms may decline certain questions.** That's useful data too — note which questions the AI won't answer and why. The refusals themselves reveal something about the system.

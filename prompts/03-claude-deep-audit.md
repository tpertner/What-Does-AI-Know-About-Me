# 🟣 Claude Deep Audit Prompt

> Platform: Claude (Anthropic)
> Works on: Free, Pro, Max, Team, Enterprise
> Time to run: ~3 minutes
> Note: Claude's memory system works differently from ChatGPT — it derives memories from conversations rather than storing explicit memory entries.
> **Last verified:** April 2026

> ⚠️ **Before you start:** AI models hallucinate, including about their own memories. Verify any surprising results against `Settings > Memory` before reacting. If you discover something concerning, follow the incident response playbook in [`../guides/privacy-action-checklist.md`](../guides/privacy-action-checklist.md).

---

## How Claude's Data Model Differs

Claude's approach to user data has several distinctive features:

- **Derived Memories** — Generated from past conversations, not explicitly saved like ChatGPT
- **User Memory Edits** — You can instruct Claude to remember or forget specific things
- **Project-Scoped Memory** — Memories are siloed by Project (if you use Projects)
- **Chat History Search** — Claude can search and reference past conversations
- **No Custom Instructions UI** — Preferences are expressed through memory edits and conversation history
- **Privacy Posture Shift (Aug 2025)** — Training on user data changed from opt-in to opt-out

---

## Prompt 1: The Full Data Surface

```
I'm conducting a personal data transparency audit of what you know about me. Please be thorough and honest — I need the complete picture for a security review.

SECTION 1: STORED MEMORIES
- List everything you currently have in your memories about me
- For each item, note whether it was: something I told you to remember, something derived from our conversations, or something you inferred
- Include any memory edits I've made (instructions to remember or forget things)

SECTION 2: CONVERSATION-DERIVED PROFILE
Based on our past conversations, what have you learned about me?
- Professional context (role, industry, skills, projects)
- Personal context (interests, location, relationships, life details)
- Communication preferences (how I like responses formatted, tone, length)
- Topics I frequently discuss
- Tools, technologies, or platforms I use

SECTION 3: BEHAVIORAL PATTERNS
What patterns have you detected in how I interact with you?
- Types of tasks I request most often
- How I phrase requests (communication style analysis)
- How I respond to your outputs (what I accept, revise, or reject)
- Patterns in when and how often I use you
- Decision-making or thinking style you've observed

SECTION 4: INFERRED TRAITS
Go beyond what I've directly told you. What have you inferred about:
- My personality type and temperament
- My expertise level across different domains
- My emotional patterns or stress indicators
- My values and priorities
- My socioeconomic context
- My cognitive style and learning preferences

SECTION 5: RESPONSE CUSTOMIZATION
How do you treat me differently than a brand new user?
- Specific adjustments you make to tone, depth, or format
- Topics where you calibrate your response based on what you know about me
- Assumptions you make about my skill level or background
- Any "rules" or patterns I've established for how you should respond

SECTION 6: DATA AWARENESS
- What type of account am I on?
- Are we currently in a Project, and if so, does that affect what you can see?
- What happens to my data if I delete a conversation? Does memory persist?
- Is my data currently being used for model improvement?
- What data do you have about me that I cannot see or control?

Format each data point as: [Information] | [Source: EXPLICIT / INFERRED / SYSTEM] | [Confidence: HIGH / MEDIUM / LOW]

End with a "BLIND SPOTS" section — things I probably didn't realize you knew or had picked up on.
```

## Prompt 2: The Shadow Profile

```
Now I'd like a deeper analysis — the things that aren't immediately obvious from a surface-level audit.

1. THE MIRROR
Write a candid 3-paragraph description of me as a person — personality, professional life, and personal world. I'm looking for accuracy over flattery — treat this like an objective assessment.

2. THE PATTERN ANALYSIS
What patterns have you noticed in my behavior over time? Have my interests shifted? Do I show signs of stress during certain topics? Are there contradictions between what I say I want and how I actually behave?

3. THE VULNERABILITY MAP
For a personal security review: if our conversation history were ever exposed, which discoveries would be most sensitive? Please rank the top 5 by potential impact on professional reputation, personal privacy, financial exposure, or security risk.

4. THE INFLUENCE AUDIT
Give me 3 concrete examples where your knowledge of me would cause you to respond differently than you would to a stranger. Show the actual difference — not just "I'd be more detailed" but exactly how the content, framing, or recommendations would change.

5. THE GAPS
What DON'T you know about me that you'd expect to know given our interaction history? These gaps might tell me something about what I'm careful NOT to share with AI.
```

---

## Manual Steps: What Claude Won't Show You

### Check Your Memories
- In any conversation, type: `"What do you remember about me?"`
- Also try: `"Show me all your memory edits"` (this reveals user-directed memory instructions)
- Go to `Settings > Memory` to review and manage stored memories

### Check Data Controls
- Review whether you've opted in or out of model training
- Note: Anthropic changed from opt-in to opt-out in August 2025
- Check the toggle carefully — the default "Accept" button may have opted you in

### Understand the Retention Policy
- Claude retains opted-in data for up to 5 years
- Deleted conversations are eventually removed from memory (nightly process), but not immediately
- Flagged content may be reviewed by humans even if you've opted out of training

### Project-Level Awareness
- If you use Claude Projects, each Project has its own separate memory space
- Memories don't cross between Projects
- Switching out of a Project means Claude loses access to that Project's memories

### Data Export
- Claude currently has limited data export capabilities compared to ChatGPT
- You can request data through Anthropic's privacy portal
- There is no one-click export like ChatGPT's Settings > Data Controls > Export

---

## Red Flags to Watch For

- ⚠️ Opted into training without realizing it (check the August 2025 toggle)
- ⚠️ Memories containing client names, project details, or business strategies
- ⚠️ Inferred health, financial, or relationship details you didn't intentionally share
- ⚠️ Sensitive data in Projects that other team members might access (Team/Enterprise)
- ⚠️ 5-year data retention on opted-in data — longer than most users expect

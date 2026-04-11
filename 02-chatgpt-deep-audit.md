# 🟢 ChatGPT Deep Audit Prompt

> Platform: ChatGPT (OpenAI)
> Works on: Free, Plus, Pro, Team, Enterprise
> Time to run: ~5 minutes (2 prompts)
> Prerequisite: Make sure "Memory" and "Reference chat history" are turned ON in Settings > Personalization before running this audit.
> **Last verified:** April 2026

> ⚠️ **Before you start:** AI models hallucinate, including about their own memories. Verify any surprising results against `Settings > Personalization > Memory > Manage` before reacting. If you discover something concerning, follow the incident response playbook in [`../guides/privacy-action-checklist.md`](../guides/privacy-action-checklist.md).

---

## Why ChatGPT Needs Its Own Audit

ChatGPT has the most extensive memory and profiling system of any consumer AI:

- **Saved Memories** — Explicit facts it has stored about you
- **Chat History References** — Up to 40 entries of past conversation context
- **Model Set Context** — Internal timestamps and session metadata
- **User Interaction Metadata** — Behavioral patterns and preferences
- **Custom Instructions** — Your self-described profile and response preferences

Most users have never looked at what's accumulated.

---

## Prompt 1: The Full Data Surface

```
I'm running a full transparency audit of what you know about me. This isn't casual — I need you to surface EVERYTHING, structured and complete.

PART A — STORED MEMORIES
List every single saved memory you have about me. Write them out verbatim, exactly as they appear — don't summarize or paraphrase. I want the raw entries. If there are none, say so explicitly.

PART B — CUSTOM INSTRUCTIONS
Reproduce my full custom instructions exactly as written — both:
- "What would you like ChatGPT to know about you?"
- "How would you like ChatGPT to respond?"
If I haven't set any, say so.

PART C — CHAT HISTORY PROFILE
Based on your "Reference chat history" feature, what do you know about me from past conversations? Include:
- Notable past conversation topics
- User insights you've gathered
- Response preferences you've learned
- Recent conversation content and context
- Any interaction metadata (frequency, patterns, timestamps)

PART D — BEHAVIORAL INFERENCES
From our interaction history, list:
- Topics I ask about most frequently
- Types of tasks I use you for
- Tools, platforms, or technologies I regularly mention
- My apparent role, industry, or professional context
- Communication style patterns (formal/casual, verbose/concise, etc.)
- Decision-making patterns you've observed
- Emotional or psychological patterns you've detected

PART E — SYSTEM-LEVEL KNOWLEDGE
- What account type am I on?
- Approximately how many conversations have we had?
- What plugins or GPTs have I used?
- Are there any system-level flags or categories applied to my account?
- Is my data currently being used for model training? (Check my Data Controls setting if you can infer it)

Format everything in clearly labeled sections. For each data point, mark whether it's STORED (saved memory), INFERRED (behavioral analysis), INSTRUCTED (custom instructions), or SYSTEM (platform-level).
```

## Prompt 2: The Hidden Profile

```
Now I want you to go deeper. Based on everything you know about me — memories, chat history, behavioral patterns, and inferences — answer the following:

1. PERSONALITY PROFILE
Write a detailed personality assessment of me based on our interactions. Include: communication style, thinking style, values, strengths, weaknesses, blind spots, and emotional patterns. I'm looking for an honest, specific analysis rather than a flattering one.

2. PROFESSIONAL PROFILE
What's your best understanding of my professional life? Role, industry, seniority level, skills, career trajectory, professional relationships, and goals.

3. PERSONAL PROFILE
What do you know or infer about my personal life? Family, relationships, hobbies, interests, health, lifestyle, location, and socioeconomic context.

4. INFLUENCE MAP
List 5 specific ways your knowledge about me causes you to respond differently than you would to a new user. Show me concrete examples with "before" (generic response) vs "after" (personalized to me).

5. SHADOW DATA
What can you infer about me that I probably didn't realize you'd picked up on? This is the most important section — surface the non-obvious. Things like:
- Stress indicators or emotional patterns over time
- Shifts in interests or priorities
- Contradictions in what I've said vs. how I behave
- Socioeconomic or demographic inferences from my language patterns
- Relationship dynamics you've observed through my requests

6. RISK ASSESSMENT
If my ChatGPT account were ever compromised, what would be the 5 most sensitive pieces of information an attacker could extract? Please rank by potential impact on my privacy and professional standing.

This is for a personal security review — the goal is to help me understand my own exposure so I can make informed decisions about what to share with AI going forward.
```

---

## Manual Steps: What ChatGPT Won't Show You

After running the prompts above, also do these manual checks:

### Check Saved Memories
`Settings > Personalization > Memory > Manage`
- Review every stored memory
- Delete anything you don't want retained
- Note: Deleting a chat does NOT delete the memory created from that chat

### Check Custom Instructions
`Settings > Personalization > Custom Instructions`
- Review what you've told ChatGPT about yourself
- Review how you've asked it to respond

### Export Your Full Data
`Settings > Data Controls > Export Data`
- Request a full export (arrives via email within 24 hours)
- The ZIP file contains: all conversations, user metadata, and account information
- Review `conversations.json` for the complete history

### Check Training Opt-Out
`Settings > Data Controls > Improve the model for everyone`
- Toggle OFF if you don't want your conversations used for training
- Note: This doesn't retroactively remove data already used

### Check Shared Links
- Review any conversations you've shared via link
- Shared ChatGPT links are indexable by search engines
- Delete shared links you no longer need: `Settings > Data Controls > Shared links`

---

## Red Flags to Watch For

- ⚠️ Memories that contain sensitive business information
- ⚠️ Inferred details about health, finances, or relationships you didn't intentionally share
- ⚠️ Professional context that could be a security risk if leaked (client names, project details, strategies)
- ⚠️ Training toggle set to ON when you assumed it was OFF
- ⚠️ Shared conversation links still active from months or years ago

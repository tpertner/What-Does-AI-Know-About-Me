# 🟠 Perplexity Deep Audit Prompt

> Platform: Perplexity AI
> Works on: Free, Pro
> Time to run: ~2 minutes
> Key difference: Perplexity is primarily a search engine with AI — its data model centers on search patterns rather than conversational memory.
> **Last verified:** April 2026

> ⚠️ **Before you start:** AI models hallucinate, including about their own memories. Verify any surprising results against your actual thread history before reacting. If you discover something concerning, follow the incident response playbook in [`../guides/privacy-action-checklist.md`](../guides/privacy-action-checklist.md).

---

## How Perplexity Differs

Perplexity occupies a unique position in the AI landscape:

- **Search-First Architecture** — Every query is a search, meaning Perplexity knows what you're researching
- **No Persistent Memory System** — Unlike ChatGPT or Claude, Perplexity doesn't maintain cross-conversation memory
- **Thread History** — Past search threads are saved and searchable
- **Collections** — User-organized groups of searches reveal topic clustering
- **Profile Data** — Account-level preferences and settings
- **Source Tracking** — Perplexity knows which sources you click on, trust, and return to

The risk profile is different: less about personality modeling, more about revealing your research interests, concerns, and information needs.

---

## Prompt 1: The Full Data Surface

```
I'm conducting a transparency audit of what you know about me from our interaction history. Please be thorough and structured.

SECTION 1: ACCOUNT PROFILE
What do you know about me from my account?
- Name, email, or profile information
- Account type (Free or Pro)
- Preferences or settings I've configured
- Connected integrations or services

SECTION 2: SEARCH & RESEARCH PATTERNS
Based on my search history with you:
- Topics I research most frequently
- Types of questions I ask (factual, comparative, how-to, opinion, etc.)
- Subject areas I return to repeatedly
- How my research interests have evolved over time
- Any sensitive topics I've researched (health, legal, financial, personal)

SECTION 3: BEHAVIORAL PATTERNS
What patterns have you detected in how I use Perplexity?
- How I phrase my queries (keyword-style vs. conversational)
- Whether I use follow-up questions or single queries
- How I interact with sources (do I ask for specific types of sources?)
- Preference for depth vs. speed
- Time patterns (when I tend to search)

SECTION 4: INFERRED PROFILE
Based on my search patterns, what can you infer about:
- My profession or industry
- My expertise level across different topics
- My current projects or priorities
- My personal interests and concerns
- My location or timezone
- My socioeconomic context
- My decision-making style

SECTION 5: COLLECTIONS & ORGANIZATION
- What Collections have I created?
- What do my Collections reveal about my priorities and projects?
- Are there threads I've saved or starred?

SECTION 6: DATA & PRIVACY
- Is my search history being used for model improvement?
- How long are my search threads retained?
- Can Perplexity's data about me be exported?
- What data persists after I delete a thread?

For each data point: [Information] | [Source: EXPLICIT / INFERRED / SYSTEM] | [Confidence: HIGH / MEDIUM / LOW]

End with "RESEARCH REVEALS" — what my search patterns reveal about my life, concerns, and priorities that I might not have consciously considered.
```

## Prompt 2: The Research Profile

```
Based on my complete search history with you, answer these:

1. THE RESEARCH BIOGRAPHY
If you wrote a short bio of me based solely on what I've searched for, what would it say? Write it as a paragraph — the person, their world, their concerns, their ambitions.

2. THE CONCERN MAP
What am I worried about? What problems am I trying to solve? Map my searches to underlying concerns or goals — not just the topics but the motivations behind them.

3. THE KNOWLEDGE GAPS
Based on what I search for, where are the gaps in my knowledge? What topics do I repeatedly research because I haven't fully grasped them?

4. THE SENSITIVE DISCOVERIES
If someone accessed my Perplexity history, what would be the most revealing or sensitive threads? Think about: health concerns researched, financial questions asked, relationship or personal issues explored, professional vulnerabilities exposed.

5. THE PATTERN NOBODY SEES
What's one non-obvious pattern in my search behavior — something I probably haven't noticed about myself?
```

---

## Manual Steps: What Perplexity Won't Show You

### Review Your Thread History
- Open Perplexity and review your past threads in the sidebar
- Note how far back the history goes
- Look for threads containing sensitive searches you may have forgotten about

### Review Collections
- Check any Collections you've created
- Consider whether the organization reveals sensitive project structures or priorities

### Check Account Settings
- Review your profile and preference settings
- Check whether you've connected any third-party accounts

### Data Export
- Perplexity currently has limited data export options
- Check their privacy policy for data request procedures
- You can manually delete individual threads

### Privacy Policy Review
- Perplexity's privacy practices are less established than larger platforms
- Review their current privacy policy at perplexity.ai/privacy
- Note whether they share data with third parties or use it for training

---

## Red Flags to Watch For

- ⚠️ Sensitive health, legal, or financial searches preserved in history
- ⚠️ Research patterns that reveal business strategy or competitive intelligence activity
- ⚠️ Personal searches mixed with professional searches on the same account
- ⚠️ Collections that map out confidential projects or client work
- ⚠️ Search patterns that reveal concerns you haven't shared with anyone else

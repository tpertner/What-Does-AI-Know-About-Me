# Platform Comparison: What Each AI Collects, Stores, and Shares

> **Last verified:** April 2026
> **Stability note:** AI platform policies change frequently. Cross-check against current official documentation before making compliance decisions.

---

## The Big Picture

Every AI platform collects data. The differences lie in **what** they collect, **how long** they keep it, **who** can see it, and **what** they do with it. This guide breaks down the specifics across ChatGPT, Claude, Gemini, and Perplexity.

---

## Data Collection Scope

### ChatGPT (OpenAI)

**What it collects:**
- All conversation content (prompts and responses)
- Uploaded files and images
- Account information (name, email, phone, payment data)
- Device and browser information
- IP address and approximate location
- Usage patterns (frequency, session length, features used)
- Saved memories and custom instructions
- Plugin/GPT usage history
- Feedback (thumbs up/down, written feedback)

**What it infers:**
- Communication style preferences
- Expertise level across domains
- Personality and behavioral patterns
- Professional context and role
- Response format preferences

**Unique risk:** The most extensive memory system of any consumer AI. Memories persist even when conversations are deleted.

---

### Claude (Anthropic)

**What it collects:**
- Conversation content
- Uploaded files and documents
- Account information
- Device and browser data
- IP address
- Usage patterns
- Memory edits (user-directed remembering/forgetting)
- Derived memories from conversations

**What it infers:**
- Communication preferences
- Professional context
- Expertise level
- Behavioral patterns across conversations

**Unique risk:** Data retention of up to 5 years for opted-in users. Privacy posture shifted from opt-in to opt-out for training in August 2025.

---

### Gemini (Google)

**What it collects:**
- Conversation content
- Account information (tied to Google Account)
- Device information (significantly more on mobile)
- Location data (especially on mobile)
- Contact information (on mobile)
- App usage patterns
- Cross-Google service data (when Extensions are enabled): Gmail, Drive, Calendar, Maps, YouTube
- Gemini Apps Activity logs
- Feedback and ratings

**What it infers:**
- Comprehensive life profile from cross-service data
- Communication patterns
- Professional and personal context
- Interests from YouTube and Search history
- Location patterns from Maps
- Schedule and commitments from Calendar

**Unique risk:** The broadest data surface of any AI assistant due to Google ecosystem integration. Mobile app collects significantly more than desktop.

---

### Perplexity

**What it collects:**
- Search queries and conversation threads
- Account information
- Device and browser data
- Source click patterns
- Collections and saved threads
- Follow-up question patterns

**What it infers:**
- Research interests and patterns
- Expertise areas based on query sophistication
- Current projects and priorities
- Concerns and information needs

**Unique risk:** Search patterns can reveal sensitive concerns (health, legal, financial) that you might not consciously think of as "shared data."

---

## Data Retention Comparison

| Platform | Default Retention | Minimum Retention | Can You Export? | Delete = Gone? |
|---|---|---|---|---|
| **ChatGPT** | Indefinitely | 30 days (temp chats) | Yes (full export) | No — memories persist |
| **Claude** | Until deleted | Up to 5 years (opted-in) | Limited | Memories lag ~24hrs |
| **Gemini** | 18 months | 72 hours (Activity OFF) | Yes (Google Takeout) | 72hr minimum hold |
| **Perplexity** | Until deleted | Unknown | Limited | Unclear on backups |

---

## Training Data Usage

| Platform | Free Tier | Paid Tier | Enterprise | Opt-Out Method |
|---|---|---|---|---|
| **ChatGPT** | Yes (default) | Yes (default) | No | Settings > Data Controls |
| **Claude** | Yes (default since Aug 2025) | Yes (default) | No | Settings toggle |
| **Gemini** | Yes (default) | Yes (default) | No | Activity Controls |
| **Perplexity** | Yes (default) | Yes (default) | N/A | Check current policy |

**Critical note:** "Opt-out" stops *future* data from being used. It does not retroactively remove data already incorporated into models. Once your data has been used for training, it cannot be fully extracted from the model.

---

## Human Review

All four platforms allow human reviewers to read your conversations under certain circumstances:

- **Safety reviews** — Conversations flagged by automated systems
- **Quality improvement** — Random sampling for model evaluation
- **Legal compliance** — Response to law enforcement or court orders
- **Abuse detection** — Investigating violations of terms of service

**Key point:** Opting out of training does NOT opt you out of human review for safety purposes.

---

## Third-Party Data Sharing

| Platform | Shares with advertisers? | Shares with third parties? | Plugin/Extension data? |
|---|---|---|---|
| **ChatGPT** | No | Service providers only | Plugins have separate terms |
| **Claude** | No | Service providers only | MCP servers may have separate terms |
| **Gemini** | Complex (Google ecosystem) | Within Google services | Extensions access Google data |
| **Perplexity** | Check current policy | Service providers | Limited integrations |

---

## What Happens When You Delete

### ChatGPT
- Conversation disappears from interface ✅
- Saved memories from that conversation persist ❌
- Data already used for training persists ❌
- Logs retained for 30 days for safety ❌
- Shared links remain active until manually deleted ❌

### Claude
- Conversation removed from interface ✅
- Derived memories removed (nightly batch process) ⏳
- Data used for training persists ❌
- Deleted memory logs retained up to 30 days ❌

### Gemini
- Conversation removed from Gemini Apps Activity ✅
- 72-hour minimum retention regardless ❌
- Cross-service data (Gmail, Drive, etc.) unaffected ❌
- Data used for training persists ❌

### Perplexity
- Thread removed from interface ✅
- Retention of backend data unclear ⚠️
- No guarantee of complete deletion ⚠️

---

## Regulatory Landscape (2026)

The compliance environment is changing fast:

- **EU AI Act** — Prohibited practices effective Feb 2025; high-risk system requirements phasing in through 2026
- **Colorado AI Act** — Effective June 2026; requires impact assessments for high-risk AI decisions
- **California AB 2013** — Effective Jan 2026; mandates training data transparency
- **California SB 942** — Requires AI-generated content labeling
- **Illinois HB 3773** — Effective Jan 2026; addresses AI in employment decisions
- **GDPR enforcement** — Italy fined OpenAI €15M; more actions expected
- **DOJ Bulk Data Transfer Rule** — Restricts transfers of sensitive personal data

**Bottom line:** Regulators are catching up. Understanding your AI data footprint isn't just good practice — it's increasingly a legal requirement for businesses.

# Data Export Walkthrough: Get Your Data From Every Platform

*Step-by-step instructions for exporting your data from ChatGPT, Claude, Gemini, and Perplexity.*

> **Last verified:** April 2026
> **Stability note:** Export menus and button locations change frequently as platforms update their UIs. If the steps below don't match what you see, check the platform's current help documentation.

---

## ChatGPT (OpenAI)

**Difficulty:** Easy
**Time:** 2 minutes to request, up to 24 hours to receive

### Steps:
1. Log in to ChatGPT at chat.openai.com
2. Click your profile icon (bottom left on desktop)
3. Click **Settings**
4. Click **Data Controls**
5. Under "Export Data," click **Export**
6. Click **Confirm export** in the confirmation dialog
7. Wait for an email from `noreply@openai.com` (check spam/promotions)
8. Click **Download data export** in the email (link expires in 24 hours)
9. Unzip the downloaded file

### What you get:
- `conversations.json` — Your complete conversation history
- `chat.html` — Browsable version of your conversations
- `message_feedback.json` — Your thumbs up/down feedback
- `model_comparisons.json` — A/B test responses you've rated
- `user.json` — Account metadata

### What you DON'T get:
- Saved memories (view these in Settings > Personalization > Memory > Manage)
- Custom instructions (view in Settings > Personalization)
- System-level logs and metadata
- Data already used for model training

### Pro tip:
Export your data BEFORE deleting conversations. Once deleted, conversations cannot be recovered.

---

## Claude (Anthropic)

**Difficulty:** Moderate
**Time:** Varies

### Option A: In-App Review
1. In any conversation, ask: `"What do you remember about me?"`
2. Ask: `"Show me all your memory edits"`
3. Go to **Settings > Memory** to view and manage stored memories

### Option B: Privacy Portal Request
1. Visit Anthropic's privacy portal (check anthropic.com/privacy for current link)
2. Submit a data access request
3. Anthropic will provide your data in accordance with applicable privacy laws

### What you can access:
- Conversation history (visible in the interface)
- Stored memories (Settings > Memory)
- Memory edits you've made

### What you DON'T get easily:
- Complete backend logs
- Inferred behavioral profiles
- Data flagged for safety review
- Training data contributions

### Pro tip:
Run the Claude Deep Audit prompt (prompt 03) before requesting a formal export — the audit captures inferred data that may not appear in a formal export.

---

## Google Gemini

**Difficulty:** Easy (best export experience of any platform)
**Time:** Minutes to hours depending on data volume

### Option A: Google Takeout (Comprehensive)
1. Go to **takeout.google.com**
2. Click **Deselect all** (to avoid downloading everything)
3. Scroll down and select **Gemini Apps**
4. Optionally also select: My Activity, YouTube History, Location History
5. Click **Next step**
6. Choose delivery method (email link, Drive, Dropbox, etc.)
7. Choose frequency (one-time or scheduled exports)
8. Click **Create export**
9. Wait for the export to be ready (you'll get an email)

### Option B: Activity Review (Quick)
1. Go to **myactivity.google.com/product/gemini**
2. Browse your complete Gemini conversation history
3. Click individual items to see full conversation details
4. Use the search bar to find specific conversations
5. Delete individual items or bulk delete by date range

### What you get:
- Complete Gemini conversation history
- Timestamps and metadata
- Connected service interactions (if Extensions were used)

### What you DON'T get:
- Internal model inference logs
- Cross-service profile data (you need to export each Google service separately)
- Data used for model training
- Advertising profile inferences (check adssettings.google.com separately)

### Pro tip:
Export from multiple Google services to see the full picture — Gemini alone doesn't capture how your Gmail, Drive, and Maps data feeds into AI responses.

---

## Perplexity

**Difficulty:** Limited
**Time:** Varies

### In-App Review
1. Log in to Perplexity
2. Review your thread history in the sidebar
3. Browse Collections you've created
4. Check account settings for any stored preferences

### Data Request
1. Review Perplexity's privacy policy at **perplexity.ai/privacy**
2. Look for data request/deletion options
3. Contact their support or privacy team for a formal data export
4. Under GDPR/CCPA, you have the right to request your data

### What you can access:
- Search thread history (in the interface)
- Collections
- Account profile information

### What you DON'T get easily:
- Backend search logs and analytics
- Behavioral pattern analysis
- Source interaction data (which results you clicked)
- Data shared with third parties

### Pro tip:
Manually review your thread history — search queries often reveal more about you than conversation-style interactions because they capture your raw, unfiltered questions and concerns.

---

## After Exporting: What to Do

### 1. Review for Sensitive Data
Search your exports for:
- Names of clients, colleagues, or family members
- Financial information (account numbers, salaries, budgets)
- Health-related conversations
- Legal questions or concerns
- Passwords, API keys, or credentials (yes, people paste these into AI)
- Confidential business strategies or documents

### 2. Clean Up
- Delete conversations containing sensitive data
- Clear memories that store information you don't want retained
- Remove shared links that are no longer needed
- Revoke unnecessary extensions or integrations

### 3. Lock Down Settings
- Opt out of model training on every platform
- Enable temporary/incognito chat modes for sensitive queries
- Separate personal and professional AI accounts
- Set up regular export and review cadence (monthly recommended)

### 4. Document for Compliance
If you're doing this for business purposes:
- Save exports as evidence of your data audit
- Document your opt-out decisions and dates
- Record any data deletion requests and confirmations
- Map AI data flows for your organization's privacy impact assessment

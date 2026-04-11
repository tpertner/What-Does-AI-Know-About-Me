# Privacy Action Checklist: Lock Down Your AI Footprint

*Actionable steps for individuals and organizations. Do the 5-minute version today, the full version this week.*

> **Last verified:** April 2026
> **Stability note:** Specific menu paths and setting names may change as platforms update. The underlying principles (opt out of training, review memories, separate personal and work accounts) remain the same.

---

## ⚡ The 5-Minute Audit (Do This Right Now)

- [ ] **ChatGPT:** Go to Settings > Personalization > Memory > Manage — read every stored memory
- [ ] **ChatGPT:** Go to Settings > Data Controls — check if "Improve the model for everyone" is ON (toggle it OFF)
- [ ] **Claude:** Ask Claude "What do you remember about me?" in a new conversation
- [ ] **Gemini:** Go to myactivity.google.com/product/gemini — review your stored conversations
- [ ] **All platforms:** Run the Universal Audit Prompt from this repo in your most-used AI assistant

---

## 🔒 The Full Lockdown (This Week)

### Account Hygiene
- [ ] Opt out of model training on every platform you use
- [ ] Review and delete sensitive saved memories (ChatGPT, Claude)
- [ ] Delete old conversations you no longer need
- [ ] Remove any shared conversation links (ChatGPT)
- [ ] Disable unnecessary Extensions (Gemini)
- [ ] Export your data from each platform for your records
- [ ] Review and clean up Custom Instructions (ChatGPT)

### Separation of Concerns
- [ ] Stop using personal AI accounts for work tasks
- [ ] If your company offers enterprise AI (ChatGPT Enterprise, Claude Enterprise, Gemini Workspace) — use it
- [ ] Create separate accounts for personal and professional use if enterprise isn't available
- [ ] Use temporary/incognito chat modes for sensitive one-off queries

### Sensitive Data Discipline
- [ ] Never paste passwords, API keys, or credentials into any AI
- [ ] Never paste confidential client information into consumer AI accounts
- [ ] Avoid sharing exact financial figures, account numbers, or SSNs
- [ ] Be cautious with health-related questions on non-HIPAA-compliant platforms
- [ ] Redact names and identifying details before pasting work documents

### Browser & Device
- [ ] Review browser extensions that interact with AI platforms (some scrape your conversations)
- [ ] Check mobile app permissions for AI apps (especially Gemini — location, contacts)
- [ ] Clear browser autofill data that might leak into AI conversations
- [ ] Use a privacy-focused browser or profile for AI interactions if needed

---

## 🏢 For Organizations

### Policy
- [ ] Establish a clear AI acceptable use policy
- [ ] Define which AI tools are approved for business use
- [ ] Specify what data classifications are permitted in AI tools (public, internal, confidential, restricted)
- [ ] Mandate enterprise-tier AI tools for any business use
- [ ] Require employees to opt out of model training on personal AI accounts

### Technical Controls
- [ ] Block consumer AI sites (chat.openai.com, claude.ai, etc.) on corporate networks if enterprise alternatives are provided
- [ ] Implement DLP (Data Loss Prevention) rules for AI platforms
- [ ] Monitor for shadow AI usage across the organization
- [ ] Audit AI integrations and MCP server connections
- [ ] Review API keys and service accounts connected to AI platforms

### Training
- [ ] Train all employees on AI data privacy risks
- [ ] Include AI data hygiene in onboarding processes
- [ ] Run periodic audit exercises (use this repo's prompts)
- [ ] Share real-world examples of AI data breaches and incidents

### Compliance
- [ ] Map AI data flows for privacy impact assessments
- [ ] Document AI vendor data practices and DPAs (Data Processing Agreements)
- [ ] Prepare for Colorado AI Act (June 2026) and other emerging regulations
- [ ] Maintain audit trail of training opt-out decisions
- [ ] Review AI vendor privacy policy changes quarterly

---

## 📅 Monthly Maintenance Routine

Set a recurring calendar reminder — 15 minutes once a month:

1. **Run the Universal Audit Prompt** on your most-used platform (2 min)
2. **Review saved memories** on ChatGPT and Claude (2 min)
3. **Delete old conversations** you no longer need (3 min)
4. **Check privacy settings** haven't been reset by platform updates (2 min)
5. **Scan for new shared links** or integrations you don't recognize (2 min)
6. **Check for privacy policy updates** from your AI providers (4 min)

---

## 🚨 Incident Response: What to Do If the Audit Surfaces Something Alarming

Running the audit prompts in this toolkit may reveal that an AI platform has stored, inferred, or retained information you didn't realize was there. Here's how to respond calmly and effectively.

### Step 1: Pause and Verify Before Reacting

Don't assume the AI's output is accurate. Models hallucinate — including about their own memories. Before escalating:

1. **Cross-check the claim against the platform's actual settings.**
   - ChatGPT: `Settings > Personalization > Memory > Manage`
   - Claude: `Settings > Memory` or ask *"What memory edits do you have about me?"*
   - Gemini: `myactivity.google.com/product/gemini`
   - Perplexity: Review your thread history in the sidebar
2. **If the claimed memory doesn't appear in the platform UI, it's likely a hallucination.** Treat it as such.
3. **If the claimed memory IS there, proceed to Step 2.**

### Step 2: Contain the Exposure

Once you've verified a real concern:

1. **Delete the specific conversation** immediately
2. **Delete any memories** derived from that conversation (conversation deletion alone doesn't remove memories)
3. **Request formal data deletion** through the platform's privacy portal
4. **Opt out of training** if you haven't already (this prevents future use, not past)
5. **Change any credentials** that were exposed (passwords, API keys, tokens, session tokens)
6. **Revoke any connected integrations** (plugins, extensions, MCP servers, GPTs)

### Step 3: Assess the Impact

- **Was any business data involved?** (Client names, contracts, financial figures, strategy documents, source code)
- **Was any regulated data involved?** (PII, PHI, PCI, student records, biometric data)
- **Was any third-party data involved?** (Information about people who didn't consent to being entered into AI)
- **What's the potential blast radius if this information were exposed publicly?**

### Step 4: Escalate If Needed

- **Business data involved** → Notify your security team and legal counsel
- **Regulated data involved** → Your organization may have breach notification obligations (GDPR 72-hour rule, HIPAA, state data breach laws)
- **Third-party data involved** → Consult legal counsel about disclosure obligations to affected individuals
- **Criminal exposure** (e.g., someone else's credentials, classified info) → Contact your security or compliance officer before taking any further action

### Step 5: Document Everything

Create a record for your own protection and any future investigation:

- Date/time of discovery
- Which platform was involved
- Exact prompt you ran
- Screenshots of results (store these securely, not on the cloud where AI can access them)
- Your verification steps
- Actions taken
- Who was notified and when

### Before You Share Results Publicly

⚠️ **Redact before screenshotting.** If you're writing about your findings for a blog post, social media, or a talk:

- **Remove names** (yours, colleagues, clients, family members)
- **Remove identifying details** (employer, city, project names, specific dates)
- **Remove inferred data** about anyone other than yourself (you may have consent to share your own data, not theirs)
- **Blur or cover account identifiers** (usernames, email addresses, session IDs)
- **Consider whether screenshots reveal third-party information** that you shouldn't disclose

**If you're not sure whether something is safe to share, don't share it.** An AI audit can accidentally expose information about other people who never consented to being discussed with AI in the first place.

**Reality check:** Once data has been submitted to an AI platform, complete erasure is not guaranteed. Deletion removes it from the interface and prevents most future use, but backups, logs, and training data may retain traces. The best strategy is prevention.

---

## Resources

- [OpenAI Privacy Portal](https://privacy.openai.com/)
- [Anthropic Privacy Policy](https://www.anthropic.com/privacy)
- [Google Privacy Dashboard](https://myaccount.google.com/dashboard)
- [Google Gemini Activity](https://myactivity.google.com/product/gemini)
- [Perplexity Privacy Policy](https://www.perplexity.ai/privacy)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)

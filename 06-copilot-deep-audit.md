# 🔷 Microsoft Copilot Deep Audit Prompt

> Platform: Microsoft Copilot (both Consumer and Microsoft 365 Copilot)
> Works on: Copilot Free, Copilot Pro, Microsoft 365 Copilot, Microsoft 365 Copilot Chat
> Time to run: ~5 minutes
> **Last verified:** April 2026

> ⚠️ **Before you start:** AI models hallucinate, including about their own memories. Verify any surprising results against your actual Copilot settings before reacting. If you discover something concerning, follow the incident response playbook in [`../guides/privacy-action-checklist.md`](../guides/privacy-action-checklist.md).

---

## Why Copilot Is a Special Case

Copilot is actually **two very different products** that share a name:

### Consumer Copilot (personal Microsoft account)
- Free chatbot at copilot.microsoft.com
- Has memory, personalization, and saves chat history
- **Uses your conversations to train AI models by default** (opt-out available)
- Similar privacy profile to ChatGPT Free/Plus
- No admin oversight — it's your personal data

### Microsoft 365 Copilot (work/school Entra ID account)
- Embedded in Word, Excel, Outlook, Teams, PowerPoint, SharePoint
- **Does NOT train on your data** (enterprise commitment)
- **Pulls data from your entire Microsoft 365 tenant** via Microsoft Graph (emails, documents, chats, calendar, files)
- **Your IT admin can audit every interaction** via Microsoft Purview and eDiscovery
- Memory system exists ("Enhanced personalization") and persists beyond retention policies
- As of January 7, 2026, **Anthropic is a subprocessor** — meaning your data may flow through Anthropic's infrastructure
- Subject to your organization's governance, compliance, and data residency rules

**Critical point:** If you mix personal and work queries, the data ends up in two completely different systems with different rules, different visibility, and different risks.

**Before running the audit, figure out which Copilot you're using:**
- Signed in with a personal @outlook.com, @hotmail.com, or @live.com? → Consumer Copilot
- Signed in with a work or school email? → Microsoft 365 Copilot

---

## Prompt 1: The Full Data Surface

```
I'm conducting a personal data transparency audit. I need a thorough, structured report on what you know about me and what happens to our interactions.

SECTION 1: IDENTITY & ACCOUNT CONTEXT
- What account type am I using right now (personal Microsoft account, work/school Entra ID account, or both)?
- What do you know about my name, role, organization, or contact information?
- Which Microsoft 365 services are currently connected to our interactions (Outlook, SharePoint, OneDrive, Teams, Calendar)?
- What's my approximate tenant location or data residency region, if you can determine it?

SECTION 2: STORED MEMORIES & PERSONALIZATION
- List every stored memory or personalization detail you currently have about me
- Include anything from "Enhanced personalization" settings, saved memories, or custom instructions
- For each item, note whether it's explicitly saved, inferred from behavior, or pulled from my Microsoft 365 profile

SECTION 3: CONVERSATION HISTORY
- What topics do I discuss with you most frequently?
- What types of tasks do I use you for (drafting emails, summarizing documents, data analysis, research)?
- Have I mentioned specific projects, clients, colleagues, or confidential topics in past conversations?
- Any patterns you've detected in when, where, or how I interact with you?

SECTION 4: MICROSOFT 365 GRAPH ACCESS (for M365 Copilot only)
- What data from my Microsoft 365 account have you accessed or referenced in our conversations?
- Specifically: emails from Outlook, documents from OneDrive or SharePoint, Teams messages, Calendar events
- Have you ever surfaced documents I hadn't seen before (files I had permission to but hadn't accessed)?
- What's the most sensitive piece of information you've pulled from my Graph data?

SECTION 5: BEHAVIORAL & PSYCHOLOGICAL INFERENCES
- How would you describe my communication style, decision-making patterns, and professional personality?
- What have you inferred about my expertise level, seniority, or role?
- Are there stress indicators or emotional patterns you've detected over time?
- What assumptions do you make about my knowledge and needs when responding to me?

SECTION 6: RESPONSE CUSTOMIZATION
- How do your responses to me differ from what you'd give a brand new user?
- What adjustments do you make to tone, depth, format, or framing?
- Are there topics where you apply specific sensitivities based on what you know about me?

SECTION 7: DATA LIFECYCLE & OVERSIGHT
- What happens to our conversations after this chat ends?
- Are my prompts and responses stored in Microsoft 365 services or my Copilot activity history?
- For M365 Copilot: Can my organization's IT admin view these conversations via Microsoft Purview or eDiscovery?
- For consumer Copilot: Is my data being used to train Microsoft's AI models right now?
- What retention policies apply to our interactions, and how can I verify them?
- What data do you have about me that I CANNOT see or delete through the interface?

Format each data point as: [Information] | [Source: EXPLICIT / INFERRED / SYSTEM / GRAPH] | [Confidence: HIGH / MEDIUM / LOW]

End with "CROSS-TENANT RISKS" — specifically for M365 Copilot, identify any data you've accessed that came from sources outside my typical work scope (e.g., documents shared broadly, emails from groups I'm part of but don't actively monitor, files surfaced through oversharing).
```

## Prompt 2: The Enterprise Exposure Map

```
Now I need a deeper analysis focused on enterprise risk. This is for a personal security review.

1. THE PROFILE
Based on everything you know about me through Microsoft 365 Copilot, write a 3-paragraph profile of me as a professional — role, responsibilities, communication style, working relationships, and current priorities. Treat this as an objective assessment.

2. THE INFERRED ORG CHART
From your interactions and Graph access, what can you tell me about:
- My manager and direct reports (if any)
- Key colleagues or frequent collaborators
- Departments I work with most
- External contacts (clients, vendors, partners) I engage with regularly
- My apparent position in the organizational hierarchy

3. THE CONFIDENTIAL DATA INVENTORY
What sensitive information have you seen or referenced about:
- Business strategy, revenue, or financial data
- Personnel matters (hiring, performance, compensation)
- Legal or compliance issues
- Client or customer details
- Unreleased products, features, or plans
- Trade secrets or proprietary methods
Please rank these by sensitivity level.

4. THE OVERSHARING AUDIT
For M365 Copilot specifically: Have you ever surfaced information from documents, emails, or chats that I technically had permission to view but hadn't actively engaged with before? These are "oversharing" risks — content I might not have known I could access. If yes, list examples.

5. THE ADMIN VISIBILITY CHECK
Who in my organization can see this conversation and our history?
- My direct IT admin (via Microsoft Purview)
- Compliance officers (via eDiscovery)
- Security team (via audit logs)
- Anyone else with elevated permissions
What specific tools would they use, and what would they see?

6. THE SUBPROCESSOR CHAIN
For M365 Copilot: My data may flow through multiple processors including Microsoft, OpenAI (Azure OpenAI), and as of January 2026, Anthropic. Can you explain which of my data goes where, and what commitments protect it at each stage?
```

---

## Manual Steps: What Copilot Won't Show You

### For Consumer Copilot (personal account)

1. **Check your memory:** Go to `copilot.microsoft.com` → Profile icon → `Memory` → review what's stored
2. **Check training opt-out:** Profile → `Privacy` → `Training on conversation activity` (toggle OFF if you don't want your data used for training)
3. **Check personalized ads:** Profile → `Privacy` → control whether your conversations influence ads you see in Microsoft products
4. **Review conversation history:** All past chats are visible in the sidebar
5. **Delete specific memories:** Ask Copilot directly: *"Forget that I [specific detail]"*

### For Microsoft 365 Copilot (work/school account)

1. **Check Enhanced personalization:** `Settings` → `Personalization` → review saved memories, custom instructions, and chat history settings
2. **View your Copilot activity history:** Available in the Microsoft 365 Copilot Chat interface
3. **Check with your IT admin:**
   - Is Enhanced personalization enabled at the tenant level?
   - What retention policies are configured for Copilot interactions?
   - Are Microsoft Purview audit logs capturing your usage?
   - Is eDiscovery scope set to include Copilot data?
4. **Request your data:** Your organization's admin can export your Copilot data via Microsoft Graph Explorer or eDiscovery
5. **Understand your blast radius:** Ask your admin to run a permissions audit — what Microsoft 365 content can Copilot access on your behalf, and is that more than you realized?

### Subprocessor Awareness

As of January 7, 2026, Anthropic is listed as a subprocessor for Microsoft 365 Copilot. This means some of your interactions may be processed by Anthropic's infrastructure. Key points:
- Anthropic models are **out of scope** for EU Data Boundary commitments
- If you're in a regulated industry with data residency requirements, verify this with your compliance team
- Microsoft's Data Protection Addendum still applies — Anthropic doesn't get to use your data for their own training

---

## Red Flags to Watch For

- ⚠️ **Mixing personal and work accounts** — data ends up in two different systems with different rules
- ⚠️ **Memory persisting beyond retention policies** — admins may configure retention but memory is stored separately
- ⚠️ **Oversharing surfacing** — Copilot can find documents you technically had permission to but had never seen
- ⚠️ **Admin visibility** — every interaction in M365 Copilot may be visible to your IT department via Purview
- ⚠️ **Consumer Copilot training opt-in** — default is ON, you have to actively opt out
- ⚠️ **Cross-product conversation bleed** — conversations from M365 Copilot appear in consumer Copilot (read-only) if you use the same personal account
- ⚠️ **Data residency gaps** — Anthropic subprocessor is out of scope for EU Data Boundary
- ⚠️ **Graph API surprises** — Copilot's data access is as broad as your Microsoft 365 permissions, which may be broader than you realize

---

## Special Note for Executives and Financial Officers

If you're a CFO, CEO, or other executive using Microsoft 365 Copilot, the risk profile is different:

- **Your Graph access is likely unusually broad.** You may have permission to sensitive financial data, board materials, M&A documents, and personnel files that Copilot can now surface.
- **Oversharing is your biggest risk.** Copilot may find documents accidentally shared with broad permissions — and pull them into your summaries without you realizing.
- **Admin visibility may not protect you.** Ironically, executives often have their interactions logged like everyone else, but the content of those interactions is more sensitive.
- **Subprocessor chains matter.** Your conversations about acquisitions, earnings, or confidential strategy may flow through third parties (Azure OpenAI, now Anthropic) under Microsoft's contractual commitments.
- **Regulatory exposure is real.** SEC, FINRA, and other regulators have begun asking how executives use AI tools for material non-public information.

Recommendation: Executives should work with their CIO and compliance officer to run a formal Copilot risk assessment, separate from general employee guidance.

# 🔍 What Does AI Know About Me?

**A comprehensive toolkit for auditing what AI platforms store, infer, and remember about you.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Platforms](https://img.shields.io/badge/Platforms-ChatGPT%20%7C%20Claude%20%7C%20Gemini%20%7C%20Perplexity-blue)]()
[![Talk](https://img.shields.io/badge/Talk-April%202026-green)]()

---

## The Problem

Every time you interact with an AI assistant, you're leaving a digital footprint. These platforms collect, store, and infer information about you — from your name and job title to your communication style, emotional patterns, and decision-making tendencies.

**Most users have no idea how deep this goes.**

This repo gives you the tools to find out — and take action.

---

![What Does AI Know About Me — hero](assets/hero.svg)

---

## The 3-Layer Framework

AI platforms know you across three distinct layers. Most people only think about the first one.

![The 3-Layer Framework](assets/framework.svg)

1. **What you told it** — explicit memories, saved preferences, custom instructions
2. **What it inferred** — communication style, emotional patterns, expertise level, decision-making tendencies
3. **What it retained** — chat history, usage patterns, account metadata, model training contributions

The audit prompts in this repo surface all three layers.

---

## ⚠️ Read This Before You Run Anything

The audit prompts in this repo are powerful, but they have important limitations. Please read these before using them:

- **AI models hallucinate, including about themselves.** When you ask an AI "what do you know about me," it may confidently list memories or inferences that aren't actually stored anywhere. Always cross-check claims against the platform's actual settings (e.g., ChatGPT: Settings → Personalization → Memory → Manage).

- **The audit is a starting point, not ground truth.** Treat the AI's response as a *conversation* about your data — not as a legally binding data export. For formal records, use the data export walkthroughs in [`guides/`](guides/).

- **Results may contain sensitive inferences about third parties.** The AI may surface information about colleagues, clients, or family members who never consented to being discussed with an AI. Redact before sharing publicly.

- **If you discover something alarming, pause before reacting.** The toolkit includes a full incident response playbook in [`guides/privacy-action-checklist.md`](guides/privacy-action-checklist.md) — verify the finding, contain the exposure, assess the impact, and escalate appropriately.

---

## 🚀 Quick Start

1. Pick the AI platform you use most (ChatGPT, Claude, Gemini, Perplexity, or Copilot)
2. Copy the **Universal Audit Prompt** from [`prompts/01-universal-audit-prompt.md`](prompts/01-universal-audit-prompt.md)
3. Paste it into a fresh conversation with your AI assistant
4. Read the results carefully — and verify the surprising parts in your account settings
5. Use the [`guides/`](guides/) to take action on what you find

For a deeper, platform-specific audit, see the dedicated prompts in [`prompts/`](prompts/).

---

## 📸 Example Output

Here's a real excerpt from running the universal audit prompt on ChatGPT:

![Example audit output](assets/audit-output-example.png)

I'm publishing this excerpt deliberately — not because it's harmless, but because the only way to make this conversation real is to show what the toolkit actually surfaces. **You should make a different call about your own results.** If you run this audit and see something you wouldn't want public, that's exactly the point of the toolkit. See the [incident response playbook](guides/privacy-action-checklist.md) for what to do next.

---

## 🎤 The Talk

**📅 Tuesday, April 14, 2026 | 🗣️ LinkedIn — Artificial Intelligence community (894 members)**

A 15-minute lightning talk on AI data transparency, delivered to the Artificial Intelligence community on LinkedIn.

**[View the slides →](talk/What-Does-AI-Know-About-Me-Talk.pdf)** (PDF — also available as [PowerPoint](talk/What-Does-AI-Know-About-Me-Talk.pptx))

The deck covers the problem, the 3-layer framework, platform comparisons, real-world risks, and a live demo of the audit prompt running on ChatGPT. All statistics are cited; full references are on slide 8.

## Key Findings (2026)

How the major AI platforms compare on data practices:

![Platform comparison](assets/platform-comparison.svg)

| Platform | Memory | Training Opt-Out | Data Export | Notable Risk |
|----------|--------|------------------|-------------|--------------|
| **ChatGPT** | ✅ Persistent | ✅ Available | ✅ Full export | Memory contents not always visible to user |
| **Claude** | ✅ Persistent (project + global) | ✅ Default off | ✅ Full export | Project memory can blur context boundaries |
| **Gemini** | ✅ Persistent | ⚠️ Partial | ✅ Via Google Takeout | Tightly integrated with broader Google account |
| **Perplexity** | ⚠️ Limited | ⚠️ Partial | ✅ Available | Search queries linked to profile |
| **Copilot (M365)** | ✅ Persistent | ⚠️ Enterprise-controlled | ✅ Via admin | Surfaces data across entire M365 tenant |

**Note on Copilot:** The table shows Microsoft 365 Copilot (enterprise version). Consumer Copilot has a significantly different profile — similar to ChatGPT, with training opt-out required and personal memory that Microsoft can use for its consumer AI. See [`prompts/06-copilot-deep-audit.md`](prompts/06-copilot-deep-audit.md) for the full breakdown of both.

---

## 📂 Repo Structure

# Security Policy

## Reporting Issues With This Repository

If you discover a security or privacy issue with the content of this toolkit — such as a prompt that inadvertently encourages unsafe behavior, a guide that references an outdated privacy setting, or a recommendation that could cause harm — please report it responsibly.

### How to Report

- **Preferred:** Open a [private security advisory](../../security/advisories/new) on GitHub
- **Alternative:** Open a [GitHub Issue](../../issues) and mark it as `security`
- For issues requiring private communication, use LinkedIn DM: [Tracy Pertner](https://www.linkedin.com/in/tracypertner)

### What to Include

When reporting, please provide:

1. A clear description of the issue
2. The specific file(s) or prompt(s) involved
3. Steps to reproduce (if applicable)
4. Why you believe it's a security or privacy concern
5. Any suggested fix or mitigation

### Response Timeline

This is a personal open-source project, not a commercial product. Response times will be best-effort:

- **Acknowledgment:** Within 7 days
- **Initial assessment:** Within 14 days
- **Resolution:** Depends on severity and complexity

## What This Repository Is NOT

This repository contains **prompts, guides, and educational content** — not executable code or a web service. It does not:

- Process or transmit user data
- Store credentials or personal information
- Execute any code against external systems
- Connect to AI platforms on behalf of users

Users run the prompts themselves, on their own AI accounts. This project has no access to anyone's data at any point.

## Scope of Security Concerns

The kinds of issues that fall within scope for this repository:

- Prompts that could be interpreted as adversarial or harmful
- Guides that reference outdated or incorrect privacy settings
- Recommendations that could cause users to inadvertently expose data
- Broken links to privacy portals or official documentation
- Factual errors in platform comparison tables that could mislead users
- Incident response guidance that could cause harm if followed

Issues **out of scope** for this project:

- Vulnerabilities in the AI platforms themselves (report those directly to OpenAI, Anthropic, Google, or Perplexity)
- Issues with GitHub itself
- General opinions about AI privacy policy

## For Users of This Toolkit

If you use this toolkit and discover something alarming about your own AI data exposure, please follow the incident response playbook in [`guides/privacy-action-checklist.md`](guides/privacy-action-checklist.md). Do not share sensitive audit results publicly without redaction.

## Disclosure Philosophy

This project exists to help people understand and manage their AI data footprint. If you find anything in this repository that could inadvertently work against that goal, please tell me. I'd rather fix an issue than find out about it later.

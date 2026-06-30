# AI Acceptable Use Policy (AUP) — Template
### Fill-in-the-blanks policy for a non-technical organization adopting AI/LLMs

> **How to use this template**
> - Replace every `[BRACKETED]` value with the organization's specifics.
> - Lines starting with `> 📝 Editor note:` are guidance for *you* — **delete them before publishing.**
> - Scaled for a ~50–500 person company with no dedicated AI/security team. Keep it to ~2 pages of actual policy; the notes make it look longer.
> - This is a governance artifact (Tier 3). It pairs with training (Tier 0–1) — a policy nobody understands is theater.
> - ⚠️ Not legal advice. Have `[LEGAL/COMPLIANCE CONTACT]` review before adoption, especially for regulated data (health, finance).

---

# [COMPANY NAME] — Acceptable Use Policy for AI Tools

**Effective date:** [DATE]   |   **Version:** [1.0]   |   **Owner:** [NAME / ROLE]
**Applies to:** all employees, contractors, and temporary staff using AI tools for [COMPANY NAME] work.

## 1. Purpose
This policy explains how we use AI tools (such as [APPROVED TOOL(S), e.g. Claude Enterprise]) safely and responsibly. The goal is to get the benefits of AI while protecting our clients, our data, and our reputation.

## 2. What "AI tools" means here
Any tool that generates text, images, code, audio, or analysis from a prompt — including [LIST, e.g. Claude (web, Code, Cowork)]. When in doubt whether a tool counts, ask [CONTACT].

## 3. Approved tools (use these — and only these)
- ✅ **Approved:** [e.g. Claude Enterprise — provided and managed by the company]
- ⛔ **Not approved:** any personal or free consumer AI account for company work, unless added to the approved list by [OWNER].

> 📝 Editor note: This single rule prevents "shadow AI." People go rogue when the sanctioned tool is missing or unknown — so make the approved tool easy to access.

## 4. Acceptable uses (green light)
You may use approved AI tools to:
- Draft, summarize, rewrite, or translate **non-confidential** content.
- Brainstorm, plan, and explore ideas.
- Explain concepts and help you learn.
- [ADD ROLE-SPECIFIC EXAMPLES per department.]

## 5. Prohibited uses (red light)
You must **not** use AI tools to:
1. Enter **confidential, regulated, or personal data** into any tool not approved for it (see §6).
2. Make a **final decision about a person** — hiring, firing, discipline, credit, eligibility — based on AI output alone (a human decides; see §8).
3. Generate content that is **misleading, discriminatory, harassing, or unlawful**.
4. Produce **clinical, legal, or financial advice** presented as the company's professional judgment without human review by a qualified person.
5. Bypass security controls, or paste in **passwords, keys, or secrets**.
6. [ADD: any industry-specific prohibition.]

## 6. Data rules — what you can and can't put in
We classify information in [NUMBER] levels. Only enter data into a tool **approved for that level**:

| Level | Examples | Allowed in AI? |
|---|---|---|
| **Public** | published marketing, public website text | ✅ Yes |
| **Internal** | internal memos, non-sensitive drafts | ✅ In approved tools only |
| **Confidential** | client lists, contracts, financials | ⚠️ Only in [APPROVED ENTERPRISE TOOL] per [CONTACT] |
| **Regulated / Personal** | health info (PHI), SSNs, full payment data | ⛔ Never, unless explicitly approved in writing |

> 📝 Editor note: Tie this table to the firm's real classification scheme if they have one. The simple rule to teach: **"If you couldn't email it to a stranger, don't paste it into AI you're not sure about."**
> ✅ Trust note to include if true after verifying: business data in [APPROVED ENTERPRISE TOOL] is **not used to train the provider's models** — confirm current terms in the admin console before stating this.

## 7. Verify before you rely (accuracy)
AI can sound confident and still be wrong ("hallucination"). Before using AI output in real work:
- **Check facts, figures, names, and any cited source** yourself.
- Never send unverified AI output to a client or external party.
- **You are responsible for anything you submit**, the same as if you wrote it by hand.

## 8. Human-in-the-loop (who decides)
A qualified human must review and approve AI output before it is used for:
- decisions affecting people (§5.2), client deliverables, financial actions, public statements, or [ADD].
AI assists; people remain accountable.

## 9. Fairness in hiring & HR
If AI is used to help screen or rank applicants, it may **only flag or assist** — never auto-reject — and a human makes every decision. Watch for and report biased or unfair output.

> 📝 Editor note: Connects to Tier 5 (bot/fake applications) and to legal risk. Some jurisdictions regulate automated hiring tools — flag for `[LEGAL]`.

## 10. Confidentiality & client trust
- Treat anything you put into AI as if it could be reviewed by [COMPANY NAME].
- Follow all existing confidentiality and client agreements — AI does not change them.
- **Disclosure:** [STATE the company's stance — e.g. "Tell clients when AI materially produced a deliverable, per contract terms."]

## 11. Security & reporting
- Use only company-managed accounts with [MFA / SSO] enabled.
- Be alert to AI-enabled scams (realistic phishing, voice/video deepfakes): **verify money, data, or access requests through a second channel** before acting.
- **Report** suspected misuse, data exposure, or scams to [CONTACT / CHANNEL] **immediately and without fear of blame** — fast reporting limits harm.

> 📝 Editor note: The "no blame" wording matters. Punishment guarantees silence; silence guarantees the next incident is worse.

## 12. Roles & responsibilities
- **Policy owner:** [NAME/ROLE] — maintains this policy, approves tools, answers questions.
- **Managers:** ensure their teams are trained and follow this policy.
- **Everyone:** follow the rules above and ask when unsure.

## 13. Records & retention
AI chats and outputs may be retained per [RETENTION PERIOD / SYSTEM]. Save finished work to [APPROVED STORAGE, e.g. SharePoint/OneDrive] per the team's naming convention.

> 📝 Editor note: Ties to Tier 1.5 (saving/organizing work) and Tier 3 retention.

## 14. Consequences
Violations may lead to [loss of AI access / disciplinary action per the employee handbook]. Serious or unlawful misuse may have further consequences.

## 15. Review
This policy is reviewed at least [annually / quarterly] and updated as tools and risks change. Last reviewed: [DATE].

---

## Acknowledgment
I have read and understand [COMPANY NAME]'s AI Acceptable Use Policy and agree to follow it.

Name: ______________________   Signature: ______________________   Date: __________

---

> 📝 Editor note — frameworks for credibility (don't cite in the employee version; use in the leadership pitch):
> - **NIST AI RMF** (Govern/Map/Measure/Manage) — this AUP mainly implements the *Govern* function.
> - **ISO/IEC 42001** — AI management system standard, if they ever want certification.
> - **EU AI Act** — relevant if they operate in/serve the EU; flag for legal.
> These show the policy isn't ad-hoc — it maps to recognized standards.

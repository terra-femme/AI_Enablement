# Tier 3.1 — Regulation: What Actually Applies To You
### Cutting a scary landscape down to the three questions that decide your obligations

**Audience:** leadership, legal/compliance, ops — plus anyone who has been told "we can't use AI, it's not compliant"
**Framing for the buyer:** "Most of what you've read about AI regulation doesn't apply to you. Here's how to find the part that does, in one afternoon, without a law firm."

**Teaching rules (per venture standard):** one idea per asset, demo-before-theory, rule of 3, analogy-first. Each numbered sub-module below = one standalone content asset (video / one-pager / slide).

> ⚠️ **This module dates faster than any other in the curriculum.** Every date and status below was verified **2026-08-26**. Re-verify before delivering it. AI regulation is being actively amended — the EU deferred a major deadline five weeks before this was written. Teach the *shape*, not the trivia, and say out loud that you are not giving legal advice.

---

## 3.1.0 — The single idea (the hook)

Most organizations ask **"is AI legal?"** That question has no answer.

The answerable question is: **"what are we using it FOR?"** Regulation almost never targets the technology. It targets the *decision* the technology touches.

The same chatbot is unregulated when it drafts a marketing email and heavily regulated when it screens job applicants. Nothing about the model changed. The **consequence to a human being** changed.

> **Analogy:** nobody regulates spreadsheets. They regulate what you do with one — payroll, financial reporting, clinical dosing. The tool is neutral; the use is not.

**So what / now what:** stop auditing your AI tools. Start auditing your AI *use cases*. The next three modules are the three questions that sort them.

---

## 3.1.1 — Question 1: Does it decide something about a person?

This is the highest-stakes sorting question, and it maps to how nearly every regulator thinks.

**Three tiers of consequence:**

1. **No person involved** — summarizing a report, drafting copy, cleaning a spreadsheet. Effectively unregulated. This is 80% of what most teams do.
2. **A person is involved, but a human decides** — AI drafts, ranks, or flags; a named human makes the call and can overrule. Much lighter obligations, and this is the design pattern regulators keep rewarding.
3. **AI decides about a person** — hiring, firing, credit, insurance, housing, education access, medical triage. **This is where the law lives.**

> **Analogy:** the difference between an assistant who hands you a shortlist and an assistant who mails the rejection letters while you're at lunch.

**So what / now what:** for every AI use case on your list, write which tier it's in. Tier 3 use cases need Tier 3 governance (`docs/` — acceptable-use policy, human-in-the-loop, documented criteria) *before* they go live, not after.

**Connects to:** Tier 5.1 — using AI to *rank* applicants is tier 2; using it to *auto-reject* is tier 3, and that's the line HR teams cross without noticing.

---

## 3.1.2 — Question 2: What kind of data goes in?

Regulation you were *already* subject to doesn't stop applying because there's an AI in the middle.

- **Health information (US — HIPAA)** — if protected health information touches a vendor, you need a Business Associate Agreement with that vendor. No BAA, no PHI. This is not an AI rule; it's the rule you already had.
- **Personal data of EU/UK residents (GDPR)** — lawful basis, purpose limitation, and data-subject rights still apply. GDPR also has its own long-standing rule on decisions made solely by automated processing.
- **California and other US state privacy law (CCPA/CPRA and successors)** — disclosure and opt-out obligations.
- **Financial, legal, education records** — sector rules follow the record, not the tool.

> **Analogy:** putting confidential files through a new photocopier doesn't make them less confidential. The vendor is now a party to your obligations.

**So what / now what:** the fastest compliance win available to most organizations is **not** a policy document — it's a data classification that tells people what may be pasted where. That's Tier 3.2, and it's the single highest-leverage hour in this curriculum.

---

## 3.1.3 — Question 3: Where do your users and customers live?

Jurisdiction is decided by *who you affect*, not where your office is.

### EU AI Act — status as of 2026-08-26

The risk-based structure is the part worth teaching, because it's stable even as dates move:

| Tier | Meaning |
|---|---|
| **Prohibited** (Art. 5) | Banned outright — social scoring, certain biometric categorisation, manipulative techniques. **In force since Feb 2025.** |
| **High-risk** (Annex III / Annex I) | Permitted with heavy obligations — hiring, credit scoring, education, critical infrastructure; and AI inside regulated products like medical devices. |
| **Transparency** (Art. 50) | Tell people they're talking to AI; label AI-generated content. **In force since 2 August 2026.** |
| **Minimal** | Everything else. No specific obligations. |

**The recent change everyone will ask about:** the Digital Omnibus entered into force **27 July 2026** and **deferred the high-risk deadlines** — Annex III standalone systems (hiring, credit scoring, education, critical infrastructure) to **2 December 2027**, and high-risk AI embedded in already-regulated products (medical devices, machinery, toys) to **2 August 2028**. These dates are not conditional on further Commission decisions.

**Deferred is not cancelled**, and it is the wrong lesson to draw. If you are building a hiring or credit tool now, you are building the thing that will be in scope in December 2027 — and the design decisions you make this year are the ones you'd have to unpick.

Note the asymmetry that trips people up: **transparency obligations are live right now**, while the scarier-sounding high-risk regime is not yet. The obligation most organizations actually have today is the boring one — *tell people it's AI*.

### United States — verified 2026-08-26

No single federal AI statute. Instead, three layers:

**1. Existing regulators applying existing law.** The FTC on deceptive claims, the EEOC on hiring discrimination, financial and health regulators on their own firms. *"The AI did it"* has never been accepted as a defence. This layer has applied the whole time and is the one most organizations forget.

**2. State law — where the actual movement is.** The landscape shifted hard in 2026:

| Jurisdiction | What it requires | Status |
|---|---|---|
| **NYC Local Law 144** | The only US law mandating a bias audit *by name*: annual independent audit of automated employment decision tools, publicly posted results summary, ≥10 business days' notice to candidates. Auditors test adverse impact using the EEOC's four-fifths rule. | In force |
| **Illinois HB 3773** (amends the Human Rights Act) | Disclose when AI is used in employment decisions; discrimination liability for biased outcomes; **bars using zip code as a proxy** for protected classes. | Effective 1 Jan 2026 |
| **Illinois BIPA** | Separate and still the strictest US biometric regime — notable for its **private right of action** and substantial damages. | In force |
| **California (CPPA ADMT rules)** | For significant decisions including employment: pre-use notice, opt-out, access right, appeal right, and a **pre-use risk assessment**. | Phasing in across 2026–2027 |
| **Colorado SB 26-189** | **Repealed and replaced** the 2024 Colorado AI Act (SB 24-205). Much narrower: transparency about consequential decisions, a structured adverse-action and **human review** process, and record retention for ≥3 years. A disclosure regime, *not* the original reasonable-care duty. | Signed 14 May 2026, effective **1 Jan 2027** |
| **Texas HB 149** | Among the broadest enacted state AI laws. | Enacted |

> **Do not teach the 2024 Colorado AI Act.** It was repealed. A lot of training material still circulating describes obligations that no longer exist, and quoting them is an easy way to lose a room that has counsel in it.

**3. Frameworks — voluntary, but increasingly load-bearing.** Three things get conflated constantly, and they do three different jobs:

- **EU AI Act** — *binding law.*
- **NIST AI RMF** — a *voluntary method.* Four functions: **Govern, Map, Measure, Manage.** NIST publishes crosswalk documents mapping it to ISO/IEC 42001, the EU AI Act and the OECD AI Principles, so adopting one doesn't strand you.
- **ISO/IEC 42001** — a *certifiable management-system standard.* Something you can be audited against and put in a procurement response.

**The commercially important part:** the Texas and California regimes offer **safe harbour or a rebuttable presumption of compliance** where a business has implemented a recognised framework such as NIST AI RMF or ISO/IEC 42001. That converts "voluntary best practice" into a legal shield, and it is the single strongest argument for doing governance work *before* you are compelled to.

**Federal direction of travel:** Executive Order 14110 was rescinded in January 2025 and superseded by EO 14179, and there is an active push toward a national policy framework with **federal preemption** of state AI law, alongside agency deliverables landing through 2026 (Commerce, FCC, FTC). Two cautions for teaching: this is genuinely unsettled and will have moved by the time you deliver it, and **state attorney-general enforcement under existing consumer-protection law survives regardless** of what happens to AI-specific statutes. Preemption of a state AI act is not immunity.

> **Analogy:** the EU wrote one big rulebook and keeps amending it. The US is enforcing a dozen old rulebooks against a new tool, while fifty states each draft their own. Both reach you; neither is easy to look up, and the US one changes underneath you.

**So what / now what:** two forces push the same way. If you sell to enterprises or the public sector, ISO 42001 and NIST AI RMF alignment show up in procurement questionnaires *before* any law compels them — customers become your regulator first. And where safe harbour exists, the same framework work that wins the deal also limits the liability. That is a rare alignment, and it is the argument to lead with when leadership asks why governance is worth funding now rather than later.

---

## 3.1.4 — The 90-minute compliance starter (the deliverable)

The workshop exercise. Three artifacts, one sitting:

1. **A use-case register.** Every place AI touches your work, each tagged with its consequence tier from 3.1.1. Most organizations have never written this down, and the act of writing it resolves half the anxiety.
2. **A data classification.** Three buckets: *free to use / internal only / never paste*. One page. See Tier 3.2.
3. **A named owner.** One human accountable for AI use, with the authority to say no. Not a committee.

> **The rule of 3 for leadership:** know what you're using it for, know what data goes in, know who's accountable. An organization that can answer those three is ahead of most of its peers, regulated or not.

**So what / now what:** this is deliberately not a policy document. Policies get written, filed, and ignored. A register, a classification, and an owner are things people actually use — and they're what an auditor or an enterprise customer asks for first.

---

## Delivery notes

- **Do not give legal advice.** Say it out loud, early, and put it in the deck. You are teaching people which questions to take to counsel — that's a genuinely valuable service, and it's a defensible one.
- **Lead with 3.1.1, not the EU AI Act.** Regulatory alphabet soup makes rooms shut down. The consequence-tier question makes them start sorting their own work, which is where the engagement is.
- **Expect "so we can't use AI at all?"** The answer is that most of what they want to do sits in tier 1 with no obligations attached. Regulation is a reason to be *deliberate*, not a reason to abstain — and abstaining has its own costs (see Tier 5: shadow AI is what happens when you say no).
- **Re-verify the dates every single time.** A stale deadline in a compliance deck destroys your credibility faster than not knowing.

# Tier 5 — AI-Enabled Threats & Defense
### How scammers use AI against businesses, and how to stay safe

**Audience:** everyone (awareness) + HR + finance + IT/leadership (deeper playbooks)
**Framing for the buyer:** "AI didn't just make your team faster — it made attacking you faster, cheaper, and more convincing. Here's where you're exposed and what to do Monday."

**Teaching rules (per venture standard):** one idea per asset, demo-before-theory, rule of 3, analogy-first. Each numbered sub-module below = one standalone content asset (video / one-pager / slide).

---

## 5.0 — Why AI changed the threat game (the hook)
The single idea: AI removed the **three things that used to protect you** from scams.
1. **Cost** — sending 10,000 personalized scams used to take a team; now it's one person and a prompt.
2. **Polish** — the typos and broken grammar that gave scams away are gone.
3. **Personalization** — AI scrapes LinkedIn/your website and writes a message that knows your name, role, and boss.

> Analogy: scams used to be a stranger in a bad disguise. AI gives every scammer a perfect mask, fluent in your language, who's done their homework.

**So what / now what:** the old advice ("look for spelling mistakes") is dead. New defense = **verify, don't inspect.**

---

## 5.1 — The bot job-application flood (your friend's exact problem)
**Why so many bots apply:**
- AI tools auto-generate tailored resumes + cover letters and **mass-apply** to hundreds of postings in minutes.
- Job boards reward volume; there's near-zero cost to the applicant.
- Some are job-seekers gaming the system; some are **fraudulent/fake candidates** (see 5.2).

**Why HR is drowning:** they're reviewing AI-generated volume *manually*, with no AI-assisted screening to fight fire with fire.

**Defense (HR playbook — one asset each):**
1. **Screening questions that bots fumble** — role-specific, scenario-based, or company-specific questions in the application itself.
2. **Verification gates early** — short live/async video task, or a quick phone screen, before investing review time.
3. **AI-assisted triage, done responsibly** — use AI to *rank/flag*, never to *auto-reject* (bias/legal risk). Human makes the call. (This is where Tier 3 governance connects: document the criteria, keep a human in the loop.)

---

## 5.2 — Fake & deepfake candidates (the scarier cousin of 5.1)
Not just spam — actual fraud, especially for **remote roles**:
- **Stolen/synthetic identities** applying to get on payroll or inside systems.
- **Deepfake video interviews** — real-time face/voice swaps so the person on the call isn't who they claim.
- **Documented threat:** state-sponsored **fake remote IT worker schemes** (widely reported, incl. DPRK operatives) using AI-assisted resumes and deepfakes to get hired at Western firms and exfiltrate money/data.

**Defense:**
1. **Liveness checks** — ask them to turn their head, hold up ID, do something unscripted; deepfakes still struggle with this.
2. **Verify the human ≠ verify the resume** — confirm identity through an independent channel; watch for mismatches (audio lag, lighting, refusal to go on-camera).
3. **Limit blast radius on day one** — least-privilege access for new remote hires until identity is fully confirmed.

---

## 5.3 — AI phishing & Business Email Compromise (BEC)
**What's new:** phishing emails are now fluent, personalized, and context-aware. **BEC** = the costliest version: a scammer impersonates an executive/vendor to trick someone into wiring money or sending data.
- **Spear phishing:** AI writes a targeted message using your public info.
- **Vendor/invoice fraud:** fake "updated banking details" email from a "supplier."
- **CEO fraud:** "Hey, I'm in a meeting, need you to handle a payment quickly."

**Defense (the one rule that matters most):**
1. **Out-of-band verification** — any money/data/credential request gets confirmed through a *different* channel (call a known number, not the one in the email).
2. **A no-blame "pause and check" culture** — urgency is the #1 manipulation lever; make it normal to slow down.
3. **Email authentication** — make sure IT has **SPF, DKIM, DMARC** configured (awareness-level: these help block spoofed senders).

---

## 5.4 — Voice & video deepfakes (vishing + impersonation)
The idea: a few seconds of someone's voice (from a webinar, voicemail, social post) is enough to **clone it**.
- **Voice-clone phone scams** ("it's your CEO, wire the funds").
- **Real, documented case:** a finance worker at **Arup** was tricked into paying out ~**$25M** after a video call with deepfaked colleagues. Use this as the wake-up-call story.

**Defense:**
1. **Codewords / callback protocols** for any high-value or unusual request.
2. **Never trust voice or video alone** for authorization — it is no longer proof of identity.
3. **Limit public voice/video exposure** for finance-authority staff where practical.

---

## 5.5 — Your own AI use as an attack surface (shadow AI + data leakage)
Connects to Tier 3. The threat from *inside*:
1. **Data leakage** — employees pasting confidential/PHI/secrets into unsanctioned consumer AI tools.
2. **Shadow AI** — unapproved tools nobody can see or secure.
3. **Prompt injection (awareness):** malicious instructions hidden in a document/website/email that an AI assistant then obeys. Just plant the concept — they don't need depth, they need to know AI can be *tricked by content it reads*.

**Defense:** sanctioned tools (so people don't go rogue), a clear "never paste" list (Tier 1.9), and data classification (Tier 3.11).

---

## 5.6 — The small-business defense playbook (the leave-behind)
Tie it together into one page the buyer keeps:
1. **Verify, don't inspect** — confirm identity/requests out-of-band; appearance and fluency prove nothing now.
2. **MFA everywhere** + least privilege — assume credentials will get phished eventually.
3. **A reporting path with zero blame** — fast reporting beats prevention; punishment guarantees silence.
4. **Train on a cadence** — threats evolve; one-time training is theater. Quarterly 20-minute refreshers.
5. **Money/data/access requests = mandatory second channel.** No exceptions, including for the CEO.

---

## Asset backlog from this tier
- 60-sec video: "Why are bots applying to your jobs?" (5.1)
- One-pager: "HR's 3-step fake-candidate screen" (5.1 + 5.2)
- The Arup $25M deepfake story as a 2-min wake-up talk (5.4)
- Leave-behind one-pager: "5 rules that stop AI scams" (5.6)
- Lunch-and-learn deck: "How scammers use AI against your business" (whole tier, ~30 min)

> Accuracy note before publishing: re-verify named cases (Arup ~$25M deepfake; DPRK fake-IT-worker schemes) against current reporting, and cite sources in any public content.

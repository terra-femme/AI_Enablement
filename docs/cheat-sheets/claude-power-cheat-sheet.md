# Claude Power Cheat Sheet
### Get exceptional results — a one-page reference for everyday work

> Mindset: **you're delegating to a brilliant new colleague, not searching a database.** Brief it well, check its work.
> ⚠️ Never paste anything you couldn't email to a stranger into a tool you're not sure about. Verify facts before you send.

---

## 1. The prompt recipe — **CREF**
Most "bad AI answers" are really bad *briefs*. Give it four things:

| | Means | Example phrase |
|---|---|---|
| **C — Context** | the situation | "A client is upset their report is 3 days late." |
| **R — Role** | who Claude should be | "You're a calm, accountable account manager." |
| **E — Example** | your tone/sample (optional, powerful) | "Match the tone of this past email: …" |
| **F — Format** | the shape you want back | "3 short paragraphs, warm, end with a clear next step." |

**Before:** *"Write an email to a client about a delay."* → generic.
**After (CREF):**
> *"A client is upset their report is 3 days late (context). You're a calm, accountable account manager (role). Match the warm tone of the email I'm pasting below (example). Write 3 short paragraphs — acknowledge, explain briefly without excuses, give a firm new date — no jargon (format)."*

**If the answer's off, don't restart — steer it:** "shorter," "more formal," "add a deadline," "remove the apology in line 2."

---

## 2. Priming (set it up before you ask)
Priming = the standing context you give *before* the task so every answer fits you.

- **Quick priming (in the message):** start with role + audience + constraints.
  > "Act as our compliance reviewer. Audience is non-technical staff. Flag risks plainly, cite the policy section."
- **Persistent priming (best):** put it in a **Project's custom instructions** so you don't retype it every time (see §4).
- **Few-shot priming:** show 1–2 examples of good output. Claude mirrors patterns fast.
  > "Here are two approved subject lines we like: […]. Write five more in that style."

---

## 3. Result intention (say what 'done' looks like)
Tell it the **outcome and the format**, not just the topic. Be specific about length, structure, audience, and tone.

| Vague | Intentional |
|---|---|
| "Summarize this." | "Summarize this in 5 bullets a busy exec can read in 20 seconds." |
| "Make a plan." | "Give a 30/60/90-day plan as a table: phase, goal, owner, success metric." |
| "Improve this email." | "Tighten this to under 120 words, keep the friendly tone, no buzzwords." |

> Power move: end with **"Before you write, ask me 3 questions if anything is unclear."** Catches wrong assumptions early.

---

## 4. Project folder contents (set up a Project once, reuse forever)
A **Project** = a saved workspace: **custom instructions + uploaded reference files (knowledge)** + its chats. Make one per recurring job.

**Example — a "Client Communications" Project should contain:**
- **Custom instructions:** "You write client emails for [Company]. Tone: warm, professional, concise. Never promise dates without a placeholder for me to confirm. Avoid jargon."
- **Knowledge files (upload):**
  - Brand/voice guide (1–2 pages)
  - 3–5 approved past emails (good examples)
  - Service descriptions / FAQ
  - The do-not-say list (legal/compliance phrases to avoid)
- **Result:** every chat in that Project already "knows" your voice and rules — no re-priming.

> Keep knowledge files **small, clean, and current.** Outdated or bloated files = worse answers. Remove drafts you don't want it to imitate.

---

## 5. Retrieval (make it use *your* documents, not its memory)
"Retrieval" = Claude pulling answers from files/data you give it, instead of guessing from training.

**How to do it:**
- **Attach a file** to a message, or add it to a **Project's knowledge**, then ask about it.
- **Ask in a way that forces retrieval:**
  > "Using only the attached policy, answer: what's our refund window? Quote the exact sentence and section."
- **Always make it cite:** "Quote the source line." If it can't quote it, it may be guessing — verify.

**Example:** upload the 12-page vendor contract →
> "From the attached contract only: list every deadline and who's responsible, as a table. If something isn't stated, write 'not specified' — don't infer."

---

## 6. MCPs / Connectors (give Claude access to live tools & data)
**ELI5: USB-C for AI** — a plug that lets Claude reach outside tools (email, calendar, drive, etc.).
- In **Claude Enterprise (web)** these are **Connectors / Integrations**, turned on by your **admin** (e.g., Google Drive, Gmail, Calendar).
- Once enabled, just ask naturally:
  > "Find the contract in our Drive folder 'Vendors 2026' and summarize the payment terms."
  > "Draft a reply to the latest email from [name] declining politely, and save it as a draft."
- ⚠️ Connectors expand what AI can touch → **a security decision.** Use only what your admin enabled; never connect personal accounts for work.
> 🔎 Ask your admin which connectors are turned on for your team before relying on them.

---

## 7. Skills (saved playbooks for repeat jobs)
**ELI5: a recipe Claude pulls off the shelf** — a packaged set of instructions/steps for a specific task, so results stay consistent across the team.
- Use a skill when you do the **same multi-step job repeatedly** (e.g., "turn meeting notes into our standard summary format").
- For your team: capture your best repeatable workflow once, save it as a skill/Project template, and everyone gets the same quality.
> 🔎 Skill availability depends on your plan/setup — ask your admin or [your friend, the AI lead] to set one up.

---

## 8. The 6 habits of people who get great results
1. **Brief it like a person** (CREF) — context beats cleverness.
2. **Prime once** in a Project — stop retyping your setup.
3. **State the finished shape** — length, format, audience.
4. **Feed it your documents** and make it **quote** them.
5. **Iterate, don't restart** — "fix this part."
6. **Verify + stranger test** — you own what you send; protect the data.

---

## Copy-paste starters
**General task:**
> "Context: ___. You are ___ (role). Audience: ___. Give me ___ (format/length). Tone: ___. Before writing, ask me up to 3 questions if anything's unclear."

**Document Q&A:**
> "Using only the attached file, answer ___. Quote the exact source line. If it's not in the document, say 'not specified.'"

**Make it better:**
> "Rewrite the above to be [shorter/warmer/more formal]. Keep [X]. Remove [Y]. Under [N] words."

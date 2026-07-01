# Claude Power Cheat Sheet
### Get exceptional results — a one-page reference for everyday work

> Mindset: **you're delegating to a brilliant new colleague, not searching a database.** Brief it well, check its work.
> ⚠️ Never paste anything you couldn't email to a stranger into a tool you're not sure about. Verify facts before you send.

## 🛑 The #1 rule — **DTAI: Don't Trust AI**
> - **Fact-check every number** against current, real data — AI can be confidently wrong.
> - **Always read and revise** — never send raw AI output.
> - **Use your own judgment** — you are the expert in the room.
> - **AI drafts; a human owns the final product.** It helps you start, it does not replace you.

*Everything below makes the AI a better assistant. DTAI keeps you the one in charge.*

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

## 3a. Voice & direction — be the director (and be specific)
Stop *typing a search*. Start **directing a performance.** The AI is a world-class actor who will do exactly what you describe — so describe it like an **Oscar-winning Shakespearean director**: set the scene, name the mood, shape the pacing. Think in **vivid, concrete detail — like a page of Stephen King**: specific, textured, nothing vague. The richer your direction, the closer the performance.

**Flat vs. directed:**
| Flat | Directed (with voice) |
|---|---|
| "Write a follow-up email." | "Open warm but brisk — a trusted advisor who respects their time. Two tight paragraphs: first, acknowledge the delay plainly, no groveling; second, a confident next step with a firm date. Land on reassurance, not apology. Tone: calm, senior, human." |

### Make it READ and UNDERSTAND before it acts
Don't let it perform a script it hasn't studied. Direct it to read first:
> "First, **read the attached report in full** and tell me in 3 bullets what it covers and how it's structured. Write nothing else yet — I'll confirm before we continue."

This proves it actually understood the material before it produces anything (and catches misreads early).

### Point to the *exact* spot (specificity in files)
Precise references beat "fix the part near the middle" — the AI can't guess which piece you mean. Name the location:
- "Look at how **line 67** phrases the risk disclaimer — copy that exact tone in the new section."
- "In **Q1_Report.xlsx**, cell **B12** has the formula I want — apply that same logic to column C."
- "Match the structure of the **third paragraph on page 2** of **brand_guide.pdf**."
- "The row where **Region = West** looks wrong — recheck that calculation only."
- "Rewrite **bullet 2 under 'Risks'** — leave the rest untouched."

> **Director's toolkit:** set the scene → name the tone → describe the pacing → **point to the exact line/cell/section** → say what 'great' looks like. Bonus: the more specific your direction, the easier it is to **verify** you got exactly what you asked for.

---

## 3b. Plan before you build — ask what it *thinks* first
Don't let it produce the whole thing on the first swing. Make it show its **plan**, then agree on it. This catches a wrong direction in 20 seconds instead of after three wasted pages.

- **Ask for the approach, not the answer:**
  > "Before you write anything, tell me how you'd approach this — the steps you'd take and what you need from me. Don't start yet."
- **Converse and work out the kinks:** correct its assumptions, fill in missing context, agree on the outline — *then* say "looks good, go ahead."
- **Why it's imperative:** AI will confidently run the wrong way if you let it. Two minutes agreeing on a plan saves rewriting the whole output — and it surfaces the questions you forgot to answer.

**The "Plan" feature.** Some Claude tools have a dedicated **Plan mode**: the AI researches and lays out a step-by-step plan *without doing the work yet*, and you approve it before it executes. It exists to stop the AI from charging ahead and to keep **you** in control of the direction. 🔎 Availability depends on the tool/plan (it's standard in the developer tool, Claude Code) — ask your admin/AI lead if it's on in your workspace. Even without the button, the habit is the same: **plan → approve → execute.**

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

### 5a. Working with attachments — refer to them clearly
**Attach vs. paste:** attach **files** (PDF, Word, Excel, slides, images/screenshots). **Paste** short snippets of text directly. Don't paste a huge document as text when you can attach the file.

**Refer to attachments by name — especially with more than one.** Vague references ("the document") confuse Claude when several files are attached.
- One file: *"In the attached file, …"* is fine.
- **Multiple files: name each one.**
  > "Compare **Q1_Report.pdf** and **Q2_Report.pdf** — list what changed in revenue. Use **brand_guide.pdf** for the tone of your summary."
- **Point to the part you mean:** "see page 3," "the table under 'Pricing'," "the second screenshot."

**Tell Claude what to *do* with each attachment** (its role):
> "Use **contract.pdf** as the source of facts, **email_examples.docx** as the tone to copy, and **checklist.xlsx** as the format to fill in."

**Images & screenshots:** you can attach them and ask Claude to read/describe/extract.
> "From the attached screenshot, type out the error message exactly and explain it in plain English."

**Good habits:**
- **Name files clearly before uploading** (`Acme_MSA_2026.pdf`, not `scan_0012.pdf`) — clear names = clearer references.
- **State scope:** "using only the attached files" stops it from mixing in guesses.
- **Confirm it loaded:** if unsure, ask *"List the files you can see and one line on each"* before the real task.
- ⚠️ Same data rule applies to attachments: **don't upload confidential/regulated files** into a tool not approved for them.

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

## 🧠 How AI "memory" works — context windows (and why it forgets)
Picture the AI's short-term memory as a **whiteboard of a fixed size.** Everything in your current chat — your messages, its replies, and any attached files — gets written on it. That size limit is called the **context window.**

- **While there's room:** it "remembers" everything earlier in the chat.
- **When the whiteboard fills up:** the oldest notes get erased or condensed to make room — so in a long conversation it can **forget details from the beginning** or seem to "lose the plot."
- **Each new chat starts on a blank whiteboard** — it generally doesn't remember your previous chats (unless the info lives in a **Project's knowledge**, you paste it back in, or your tool has a cross-chat memory feature 🔎).

**What to do about it:**
1. **One topic per chat.** Start a fresh chat for a new task — cleaner, less drift.
2. **Put durable info in a Project** (custom instructions + knowledge files) so it's always available instead of trapped in one chat.
3. **Re-anchor long chats:** paste the key facts again, or ask *"summarize what we've agreed so far"* and carry that summary forward.
4. **Watch for the tell:** if it turns vague or contradicts earlier points, the window is likely full — start fresh and paste in the summary.
5. **Don't over-stuff:** attaching huge files also eats the window — attach only what's relevant.

---

## 8. The 6 habits of people who get great results
1. **Brief it like a person** (CREF) — context beats cleverness.
2. **Prime once** in a Project — stop retyping your setup.
3. **State the finished shape** — length, format, audience.
4. **Feed it your documents** and make it **quote** them.
5. **Iterate, don't restart** — "fix this part."
6. **DTAI — Don't Trust AI** — fact-check numbers, read & revise, use your judgment; you own the final product. (Plus the stranger test: protect the data.)

---

## 9. Worked example — "make this quarter's report like last quarter's" (Excel)
A full walk-through that ties every habit together. **Goal:** recreate a familiar Excel report with new numbers, in the same format — without rebuilding it by hand.

**The situation:** You have last quarter's polished sales report (`Q1_Sales_Report.xlsx`) and this quarter's raw export (`Q2_raw_data.xlsx`). You want Q2 to look and calculate exactly like Q1.

### Step 1 — Prime (tell it who to be + the goal)
Set the role and intent *before* the task:
> "You're a meticulous sales analyst. I need to produce our quarterly sales report. I'll give you last quarter's finished report as the **template/format to copy**, and this quarter's **raw data** to fill it with. Match the previous format exactly."

### Step 2 — Upload / attach the right files
Attach **both**:
- `Q1_Sales_Report.xlsx` → the **format example** (what "done" looks like)
- `Q2_raw_data.xlsx` → the **source of the new numbers**
> 💡 Attach the real **files** (don't paste thousands of rows as text). Name them clearly *before* uploading.

### Step 3 — Reference each attachment by name **and give it a role**
This is the key move — say which file does what:
> "Use **Q1_Sales_Report.xlsx** as the layout, column order, and formatting to copy. Pull all the actual numbers from **Q2_raw_data.xlsx**. Don't mix Q1's numbers into the Q2 report."

### Step 4 — State the intended result precisely
Spell out structure, calculations, and format:
> "Build the Q2 report with the **same columns and sheet layout as Q1**: Region, Units Sold, Revenue, % of Total, and a **% change vs Q1** column. Include a **totals row** at the bottom. Sort by Revenue, highest first. Give me a clean table I can paste into Excel, and list any Q2 regions that didn't appear in Q1. If a number isn't in the raw data, write 'not available' — don't estimate."

### Step 5 — What you get & how to use it
- Claude returns the **finished table** (with the calculations done) to paste straight into your sheet.
- 🔎 If **file creation / the analysis tool** is enabled in your workspace, you can also ask: *"Give me this as a downloadable .xlsx formatted like Q1."* (Availability depends on your plan — ask your admin.)

### Step 6 — Iterate, then VERIFY
- Iterate, don't restart: *"Add a grand-total row,"* *"format Revenue as currency,"* *"the % change should be (Q2−Q1)/Q1."*
- ⚠️ **Always spot-check the math** on any financial report before sending it — pick 2–3 rows and confirm the totals and % changes by hand. You own the numbers.
- ⚠️ **Data rule:** only upload these files if the report data is approved for your AI tool (no regulated/confidential data in an unapproved tool).

> **The pattern to remember:** *Prime the role → attach format + data → name each file's job → specify the exact output → iterate → verify the numbers.* That sequence works for slides, letters, and dashboards too — not just Excel.

---

## Copy-paste starters
**General task:**
> "Context: ___. You are ___ (role). Audience: ___. Give me ___ (format/length). Tone: ___. Before writing, ask me up to 3 questions if anything's unclear."

**Document Q&A:**
> "Using only the attached file, answer ___. Quote the exact source line. If it's not in the document, say 'not specified.'"

**Make it better:**
> "Rewrite the above to be [shorter/warmer/more formal]. Keep [X]. Remove [Y]. Under [N] words."

**Report like a past one (Excel/docs):**
> "Use **[old_file]** as the format/template to copy and **[new_data_file]** as the source of numbers. Rebuild it with the same columns and layout, add a totals row, and a '% change vs prior' column. Give me a table to paste into Excel. If a value isn't in the data, write 'not available' — don't estimate."

**Direct it (read first, then point to the exact spot):**
> "First read the attached **[file]** fully and tell me in 3 bullets what it covers — write nothing else yet. Then: look at **[line/cell/section, e.g. line 67]** — I want you to [copy that tone / apply that formula / match that structure] in **[target]**, and leave everything else untouched."

---

## 🏁 The capstone — a perfect prompt (Director of Sales)
Everything on this page, in one real moment.

**The scene.** It's 9:10 Monday, the last week of Q2. Your VP just messaged: *"Need a Q2 readout for the 2pm leadership meeting."* You have your CRM export (`Q2_pipeline_export.xlsx`) and last quarter's board deck (`Q1_board_readout.pptx`).

**The problem.** Your team of 8 reps hit **82% of target** — a miss. You need to explain *why*, what's recoverable in Q3, and a concrete recovery plan — in under an hour, formatted the way leadership already expects. Building it by hand would eat your whole morning.

**How AI helps.** It reads the data, drafts the narrative and a recovery-plan table in the board's format, and hands you a first draft to sharpen. *You* verify the numbers and supply the judgment (**DTAI**).

**The perfect prompt** (notice how it stacks every technique):
> *"You're my sharpest sales analyst and I'm the Director of Sales prepping a leadership readout — be concise, honest, and boardroom-calm. **First, read both attached files and tell me in 3 bullets what each contains — write nothing else until I confirm.**
> Roles: use **Q2_pipeline_export.xlsx** as the source of all numbers, and **Q1_board_readout.pptx** as the exact format, tone, and slide structure to match.
> Then draft a Q2 readout with: (1) a 3-sentence honest summary of why we hit **82% of target** — no spin, no blame; (2) a table of results by rep and by region with **% change vs Q1**; (3) a Q3 recovery plan as a table — action, owner, expected impact, deadline. **Look at how slide 4 of the Q1 deck frames the 'Risks & Actions' section and mirror that structure.** Where a number isn't in the export, write 'not available' — never estimate. Keep it to one page I can drop into the deck."*

Then: iterate (*"tighten the summary,"* *"make the recovery table more specific"*), and **fact-check every figure against the export before it goes anywhere.**

**🎙️ Voice it, don't type it.** A brief this detailed is ~150 words — that's **~40 seconds spoken vs. several minutes typed.** Use the voice/dictation button and just *talk* it through like you're briefing your analyst across the desk. Speaking naturally also tends to produce richer, more specific direction than typing — you say the details you'd skip with your thumbs. (Then glance over the transcribed text for any misheard names/numbers before you send — **DTAI** applies to your own dictation too.)

> **This is the whole cheat sheet in one prompt:** primed role → read & understand first → files named with roles → precise result intention → directed with voice → pointed to the exact slide → 'don't estimate' guardrail → iterate → verify. Master this shape and you can direct AI through almost any business task.

# Tier 3.2 — Privacy: What To Share, What Never To, and Where the AI Actually Runs
### The one-page rule your team will follow, and the local-vs-cloud question underneath it

**Audience:** everyone (the classification) + IT/leadership (the local-vs-cloud decision)
**Framing for the buyer:** "Your team is already pasting things into AI. The only question is whether they've been told what's off-limits. That's a one-page fix, and it's the cheapest risk reduction available to you."

**Teaching rules (per venture standard):** one idea per asset, demo-before-theory, rule of 3, analogy-first. Each numbered sub-module below = one standalone content asset (video / one-pager / slide).

---

## 3.2.0 — The single idea (the hook)

Everyone asks: **"Is it safe to use AI?"**

Wrong question. It produces either paralysis or a shrug, and both are expensive.

The right question is: **"Safe with what?"**

Nobody would ask "is email safe?" You already know the answer depends entirely on what you put in the email. AI is the same, and your team already intuitively understands the concept — they've just never been given the buckets.

> **Analogy:** you don't have one rule for filing cabinets. You have a drawer anyone can open, a drawer that locks, and a safe. Nobody finds that confusing. AI needs the same three drawers.

**So what / now what:** the deliverable from this whole module is one page with three lists on it. Not a policy. A page people can actually keep open.

---

## 3.2.1 — The three drawers (the core asset)

**Drawer 1 — Free to use.** Public information, anything already on your website, generic professional work, hypotheticals, anonymised examples, your own drafts. *This is most work.* Say so loudly — people over-restrict themselves and quietly lose the productivity you're paying for.

**Drawer 2 — Internal only, approved tools only.** Non-public business information: internal docs, unreleased plans, financials, non-sensitive customer records. Allowed **only** in the tool your organization has an agreement with — not a personal account, not a free tier, not a browser extension nobody vetted.

**Drawer 3 — Never paste.** The list should be short enough to memorise:

- **Credentials** — passwords, API keys, tokens, connection strings
- **Regulated personal data** — health records, government IDs, full payment card numbers, biometrics
- **Anything under legal privilege or an NDA that names disclosure limits**
- **Other people's personal data** you have no basis to share — the CV pile, the customer list

> **Analogy:** drawer 3 is the "would this be a headline?" test. If a screenshot of this prompt appearing in a news story would end someone's week, it doesn't go in.

**So what / now what:** print it. One page. In the onboarding pack. The organizations that get breached aren't the ones with a bad policy — they're the ones whose staff never saw one.

**Connects to:** Tier 5 — shadow AI. If drawer 2 has no approved tool in it, your staff will use their personal accounts for drawer-2 work, and you'll have created the exact exposure you were trying to prevent.

---

## 3.2.2 — "Does it train on our data?" is three questions wearing a trench coat

This is the question every executive asks, and it's the one most vendors answer imprecisely. Teach people to split it:

1. **Training** — will my content be used to improve the model itself? Consumer tiers and business tiers commonly differ here, and this is the question people *mean*.
2. **Retention** — how long is my content stored, and where? Different from training. Content can be stored briefly for abuse monitoring without ever touching training. Enterprise agreements often allow configurable retention, up to and including **zero-data-retention** arrangements.
3. **Access** — who at the vendor could read it, under what circumstances, and is that logged?

A vendor can honestly say "we don't train on your data" while retaining it for 30 days. Both facts are fine. What's not fine is a buyer who thought they'd asked one question and got the answer to a different one.

> **Analogy:** "does the gym keep my stuff?" — is your bag in a locker (retention), does anyone open it (access), and do they copy what's inside for their catalogue (training)? Three different answers, three different risks.

**So what / now what:** get all three in writing, at your tier, for the specific product. And note that the answer **differs between the consumer app and the business/enterprise product from the same vendor** — a staff member's personal account is governed by different terms than your contract. That gap is where most accidental exposure actually happens.

---

## 3.2.3 — Local vs cloud AI: what genuinely differs

The most common misconception in this entire curriculum: **"local means private, cloud means risky."** It's a useful instinct and an unreliable rule.

| | **Cloud AI** (Claude, and the major providers) | **Local / self-hosted AI** (open-weight models on your hardware) |
|---|---|---|
| Where your data goes | To the vendor, under contract | Stays on your machine or your network |
| Capability | The frontier — the strongest models are cloud-only | Meaningfully behind at equivalent cost; gap narrows every year |
| Cost shape | Per use — scales with usage, near-zero to start | Hardware and staff up front, cheap per query after |
| Who secures it | The vendor, audited, with certifications you can point to in procurement | **You.** Patching, access control, backups, physical security |
| Compliance posture | Contract, DPA/BAA, certifications, configurable retention/residency | No third party in scope at all |
| Fails when | You can't lawfully send the data out, or you need an air gap | You need frontier capability, or you can't staff the ops |

**The trap:** an unpatched local model on a box under someone's desk, with no access control and no logging, is **less** secure than a contracted cloud vendor with SOC 2, an enterprise agreement, and zero data retention. "It never left the building" is not a security control. Self-hosting doesn't remove the risk; it **transfers the risk to you**, and you have to actually pick it up.

**Where local genuinely wins:** true air-gapped environments, data you are legally barred from transferring, extremely high-volume repetitive tasks where per-use pricing dominates, and settings where "no third party, ever" is a hard requirement rather than a preference.

**The middle ground most organizations actually want:** cloud models with enterprise data terms — no training on your content, contractual retention limits, and **data residency controls that let you pin which geography inference runs in**. That last one is increasingly available and is often the real answer to "our data can't leave the EU." Similarly, the major clouds each offer Claude through their own platforms (AWS, Google Cloud, Microsoft), which for many organizations means the AI runs inside a vendor relationship, procurement path, and compliance boundary they've *already* approved.

> **Analogy:** local vs cloud is not "own vs rent." It's a private car versus a chauffeured one. The private car never has a stranger in it — but you're now responsible for the brakes, the insurance, and the MOT. Some people should absolutely own the car. Most just needed to know the driver is licensed.

**So what / now what:** the question isn't "local or cloud." It's *"which drawer is this data in, and does any cloud arrangement exist that covers it?"* For drawer 1 and most of drawer 2, the answer is yes and local is an expensive detour. For genuine drawer-3 workloads, local may be the only option — and then you must budget for the security work you just took on.

---

## 3.2.4 — The 60-minute deliverable

1. **Fill in the three drawers** with your organization's actual examples — not generic ones. "Our Q3 forecast" lands; "confidential business information" doesn't.
2. **Name the approved tool for drawer 2.** If there isn't one, that's the finding. Shadow AI is the guaranteed consequence of a drawer with no tool in it.
3. **Ask your vendor the three questions from 3.2.2** — training, retention, access — and file the answers where procurement can find them next year.

> **The rule of 3 for staff:** public is fine, internal goes in the approved tool only, and secrets never go in at all.

**So what / now what:** this page does more real risk reduction than any policy document, because it's the only artifact in the governance stack that a busy person will actually read to the end.

---

## Delivery notes

- **Lead with permission, not prohibition.** Open by telling people how much they *are* allowed to do. A session that starts with a list of bans gets you compliance theatre and shadow AI; a session that starts with "most of this is fine, here are the three things that aren't" gets you adoption *and* the boundary.
- **The local-vs-cloud module sells consulting.** It's the one where leadership realises they have an actual decision to make with a cost attached. Don't answer it in the room — scope it.
- **Vendor terms change.** Date the answers you collect in 3.2.2 and re-ask annually. An answer from two years ago is not evidence of anything.
- **Pairs with Tier 3.1.** Regulation tells you which drawer the law thinks something is in; this module tells your team what to do about it on a Tuesday.

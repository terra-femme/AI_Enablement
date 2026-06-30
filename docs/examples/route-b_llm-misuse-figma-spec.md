# Route B Example — Figma MCP design spec
### Same topic (misuse of LLMs), built as an *editable, reusable* Figma design

**Route A** gives you a finished image. **Route B** gives you a structured, design-system-backed
file you can restyle, theme, and reuse across a whole series. This file is the **input** you
(or Claude via the Figma MCP) feed in to generate it.

> ⚠️ **Status note:** the Figma account connected to this session (*Terra*) is on a **View seat /
> Starter tier**, which is **view-only** — the MCP cannot create or edit a file with it. To run
> Route B live you need an **Editor seat** on a Figma file. Once connected, hand Claude the
> "Generation prompt" below and it will build the frame using these tokens.

---

## 1. Design tokens (define once → reuse across the whole content series)

**Color**
| Token | Hex | Use |
|---|---|---|
| `bg/base` | `#0E1126` | frame background |
| `surface/card` | `#151A36` | item cards |
| `text/primary` | `#EEF1FF` | headings/body |
| `text/muted` | `#9AA3C7` | secondary text |
| `accent/amber` | `#F5B544` | brand accent, item 2 |
| `accent/teal` | `#46D3C2` | "fix" cues, item 3 |
| `accent/rose` | `#FF6B8A` | risk cues, item 1 |

**Type** (scale)
| Token | Size / weight | Use |
|---|---|---|
| `display` | 74 / 800 | title |
| `h2` | 34 / 800 | item titles |
| `body` | 22–26 / 400 | risk + subtitle |
| `label` | 20 / 700 caps, .18em tracking | kicker, "FIX" tag |

---

## 2. Frame + layout structure (auto-layout)

```
Frame "LLM-Misuse" (1080 x 1350, fill = bg/base, padding 72, gap 24, vertical auto-layout)
├─ Kicker  (label, accent/amber)            "AI AT WORK · RISK"
├─ Title   (display)                         "3 ways your team is quietly misusing AI"
├─ Subtitle(body, text/muted)                "Same tool, three expensive habits..."
├─ Card 1  (surface/card, radius 20, h-auto-layout, gap 28)
│   ├─ Badge "1" (rose, 96x96, radius 18)
│   └─ Stack: h2 + risk(body) + Fix chip(teal)
├─ Card 2  (… badge amber …)
├─ Card 3  (… badge teal  …)
├─ Analogy (left border accent/amber, tinted fill)
└─ Footer  (h-auto-layout, space-between): brand • "Save this · Share"
```

Make **Card** a reusable component with a variant property `accent = rose | amber | teal`, and
text fields as instance overrides → every future infographic reuses the same component.

---

## 3. Content (verbatim — the 6-line brief, filled)

1. **Purpose/audience:** LinkedIn portrait post for non-technical execs & team leads
2. **One core message:** your team is misusing AI in 3 specific, fixable ways
3. **Exact text:**
   - Title: *3 ways your team is quietly misusing AI*
   - Item 1 — **Pasting confidential data into public AI** · risk: data leaves your control · fix: *Use only sanctioned tools — never paste what you couldn't email to a stranger.*
   - Item 2 — **Trusting answers without checking** · risk: made-up info reaches clients · fix: *AI drafts, humans approve — verify before you send.*
   - Item 3 — **Treating it like a live search engine** · risk: outdated facts & invented sources · fix: *Confirm anything factual — it reasons, it doesn't "look it up."*
   - Analogy: *Think of AI as a brilliant new intern — fast, but you'd never hand it client secrets or send its first draft unchecked.*
4. **Format/size:** 1080 x 1350 portrait
5. **Style:** dark indigo, amber/teal/rose accents, clean bold sans, generous spacing
6. **Hierarchy:** title biggest → card titles → risk → fix chip → footer

---

## 4. Generation prompt (paste to Claude once Figma is editable)

> "Using the Figma MCP, create a new 1080×1350 frame called **LLM-Misuse**. First create the
> color and type variables in section 1. Build a reusable **Card** component with an `accent`
> variant (rose/amber/teal), each card containing a numbered badge, an h2 title, a muted risk
> line, and a teal 'FIX' chip. Then assemble the frame top-to-bottom per the layout in section 2,
> using the verbatim content in section 3, binding every color and text style to the variables
> (no hard-coded values). Keep it on the design system so I can theme and reuse it."

---

## Why Route B for this venture
- One Card component → the **entire Tier 0–5 infographic series** stays visually consistent.
- Swap `bg/base` to white once → instant light-mode variant for print one-pagers.
- A client can be handed the editable file to keep on-brand. Route A can't do that.

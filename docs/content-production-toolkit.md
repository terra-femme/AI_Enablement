# Content Production Toolkit
### How to actually MAKE the venture's content (videos + infographics) with AI

**Audience:** you (the creator) — this is *your* developer/creator workflow, not client-facing material.
**Purpose:** turn the syllabus (Tier 0–5) into repeatable, branded videos and infographics.

> ⚠️ Verify-before-publish: re-confirm any named MCP/tool's current status and the firm's Claude Enterprise specifics before relying on them in paid work. Links below were captured June 2026.

---

## 1. Video from React — Remotion

**Remotion** is a framework for making videos *programmatically with React*: you (or Claude) write React components, and Remotion renders them to **MP4 / WebM / GIF**. This is the "MCP that uses React to video edit" thing.

**Requirements:** Node.js + a code environment. This lives on *your* developer side — **do not teach this to the non-technical firm.**

### MCP servers / plugins that wire Claude → Remotion
| Tool | What it adds | Best for |
|---|---|---|
| **`remotion-video-mcp`** (dev-arctik) | Natural-language → scaffold project, manage scenes, sync audio, render | Plain starting point |
| **`remotion-mcp-app`** (mcp-use) | **Live inline player** — see the video render inside the chat as it edits | Iterating visually |
| **`remotion-superpowers`** (Dojo Coding) | AI voiceovers, music, stock footage, TikTok-style captions, transitions, AI review loop (5 MCP servers, 13 commands) | Production at scale |

### Why it matters for this venture
Turn **Tier 0 myth-busting scripts** and the **Arup $25M deepfake story (Tier 5.4)** directly into short, branded videos from text — a repeatable content pipeline.

---

## 2. Infographics — two routes

Pick based on whether you want a **finished image** or an **editable design file**.

| | **Route A — Claude Artifacts** | **Route B — Figma MCP** |
|---|---|---|
| How | Ask a normal Claude chat for an **SVG or HTML/CSS infographic**; export the artifact | Use Figma MCP (`generate_figma_design`, `generate_diagram`) for an editable Figma file |
| Speed | Fastest, no extra tools | Slower, but reusable |
| Best for | One-off social posts, one-pagers | Branded, reusable templates / a whole series |

---

## 3. The reusable infographic brief (fill every time)

Quality is ~90% the brief. Filling these 6 lines also enforces **one message per graphic** (fights "too much, too fast"):

```
1. PURPOSE + AUDIENCE:  e.g. "LinkedIn carousel for non-technical execs"
2. ONE CORE MESSAGE:    the single takeaway (two messages = two graphics)
3. EXACT TEXT:          headline + 3 supporting points, written verbatim
4. FORMAT + SIZE:       square 1080x1080 / vertical 1080x1350 / one-pager A4, etc.
5. STYLE:               colors (hex if branded), font feel, tone (clean/bold)
6. HIERARCHY:           what's biggest, what's secondary, what's a footnote
```

> Teaching-rule add-on: tell Claude **"rule of 3 — max 3 points, and write the everyday analogy into the graphic"** so infographics stay ELI5, not dense.

---

## 4. Recommended first builds
- Video: **"Why are bots applying to your jobs?"** (Tier 5.1) via Remotion
- Video: **The Arup $25M deepfake wake-up** (Tier 5.4)
- Infographic series: **Tier 0 myths**, one analogy per card (Route B for a reusable branded template)
- Infographic: **"Your 3 save habits"** (Tier 1.5)

---

## Sources
- remotion-video-mcp (dev-arctik): https://github.com/dev-arctik/remotion-video-mcp
- remotion-mcp-app (mcp-use): https://github.com/mcp-use/remotion-mcp-app
- remotion-superpowers (Dojo Coding): https://github.com/dojocodinglabs/remotion-superpowers
- Remotion — Prompting videos with coding agents: https://www.remotion.dev/docs/ai/coding-agents

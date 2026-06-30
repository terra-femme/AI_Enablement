# Presenter Knowledge Base
### The deeper stuff YOU need (not the AI-101 audience) — so hard questions don't rattle you

This is your study sheet for the gaps you named: MCPs, skills, differentiating tasks, personas per
task, where Claude's markdown instructions live (global vs. folders), and how this works in
enterprise. ELI5 analogies included so you can re-teach simply.

> ⚠️ **Verify-before-teach (your own rule):** product details below evolve fast. Anything marked
> 🔎 must be re-confirmed in official docs or the firm's admin console before you state it publicly.
> Concepts are stable; exact paths, model names, and enterprise toggles drift.

---

## 0. THE distinction that resolves most of your confusion
There are **two different products**, and the "markdown / config" concepts live in **different places**:

| | **Claude.ai Enterprise** (web app + Cowork) | **Claude Code** (developer CLI) |
|---|---|---|
| Who uses it | The 300-person firm — everyone | Developers / technical users |
| "Persistent instructions" | **Project custom instructions** + knowledge files | **`CLAUDE.md`** files |
| Add tools/data | **Connectors / integrations** (admin-enabled) | **MCP servers** |
| Reusable workflows | **Agent Skills** 🔎 | **Skills** (`.claude/skills/`) + plugins |
| Config location | In the web UI / admin console | Files on disk (`~/.claude/`, project `.claude/`) |

**Teaching implication:** to the firm, teach **Projects + custom instructions + connectors**. `CLAUDE.md`, `.mcp.json`, and skill folders are **Claude Code** — that's *your* developer world, not theirs. Mixing these up is the #1 way to confuse a non-technical room.

---

## 1. Differentiating tasks (model + surface selection)
**ELI5:** pick the right *worker* and the right *room* for the job.

**Surfaces (the room):**
- **Claude web (chat):** everyday writing, thinking, Q&A. Where most employees live.
- **Claude Code (CLI):** software work for developers.
- **Cowork:** agentic — give it a multi-step task and it works through it. 🔎 confirm what the firm has enabled.

**Models (the worker):** generally —
- **Opus** = most capable (hard reasoning, nuance).
- **Sonnet** = balanced (the everyday default).
- **Haiku** = fastest/cheapest (simple, high-volume).
- 🔎 Current families as of this writing: **Fable 5** and the **Claude 4.x** line (e.g. Opus 4.8, Sonnet 4.6, Haiku 4.5). **Always confirm the live lineup in-product** — names/versions change.

**Rule to teach:** *match capability to difficulty.* Don't use the heaviest model for "fix this sentence," don't use the fastest for "analyze this contract's risks."

---

## 2. "Personalities for each task" (personas / system prompts)
**ELI5:** give each job its own dedicated assistant with its own job description.

A "personality" = the standing instructions that shape how Claude behaves for a task.
- **Claude.ai Enterprise:** a **Project's custom instructions.** Make a "Compliance Reviewer" Project (formal, cites policy) separate from a "Marketing Copy" Project (punchy, on-brand). Each Project = one persona + its own knowledge files.
- **Claude Code:** the project **`CLAUDE.md`** sets conventions, and **subagents** each carry their *own* system prompt — a distinct persona per task (e.g., a "security reviewer" agent vs. a "docs writer" agent).

**Don't over-engineer it for the firm:** for them, "make a Project per recurring job and write clear custom instructions" is the whole lesson.

---

## 3. Where Claude's markdown instructions live — global vs. folders (Claude Code)
This is *your* question about `CLAUDE.md`. Claude Code reads instruction files in a **hierarchy**, and they **combine**, with more-specific / managed levels taking precedence:

| Level | Location | Scope | Checked into git? |
|---|---|---|---|
| **Enterprise / managed** 🔎 | OS-level managed path set by admins | Whole org | No (IT-deployed) |
| **User / global** | `~/.claude/CLAUDE.md` → for you: `C:\Users\aznkr\.claude\CLAUDE.md` | All *your* projects | No (personal) |
| **Project** | `<repo>/CLAUDE.md` | That project, whole team | ✅ Yes (shared) |
| **Subdirectory** | `<repo>/sub/CLAUDE.md` | Loaded when working in that subtree | ✅ Yes |

- Related: **settings** live in `~/.claude/settings.json` (you), `.claude/settings.json` (project, shared), `.claude/settings.local.json` (project, personal — gitignored).
- You can **import** other files into a `CLAUDE.md` with the `@path/to/file` syntax. 🔎 confirm syntax in current docs.

**The "most proper" convention (answering your exact question):**
1. **Global `~/.claude/CLAUDE.md`** → *your* personal cross-project preferences (how you like Claude to behave everywhere). ← this is the big file you already have.
2. **Project `CLAUDE.md` (committed)** → conventions the *whole team/project* must follow.
3. **`settings.local.json` (gitignored)** → machine-specific or private settings, never shared.
> Rule of thumb: **personal + everywhere → global; project + everyone → committed project file; private + local → `.local`.**

---

## 4. MCPs (Model Context Protocol)
**ELI5:** **USB-C for AI.** A universal plug that lets Claude connect to outside tools and data — Figma, Gmail, Drive, databases, Azure, etc.

- **What it does:** without MCP, the model only has its training + your prompt. With an MCP server, it can *act on* and *read from* real systems.
- **Claude Code config:** project-shareable `.mcp.json` at repo root, or add via `claude mcp add`; scopes are **local / project / user**. 🔎 confirm exact flags in current docs.
- **Claude.ai Enterprise equivalent:** **connectors/integrations**, enabled by an **admin** (e.g. the Gmail/Drive/Figma connectors you've seen). Same idea, admin-governed.
- **Governance flag (say this to leadership):** every MCP/connector *expands what AI can touch* → it's a security + data-governance decision, not a free-for-all. Tie to your AUP (`../acceptable-use-policy-template.md`).

---

## 5. Skills
**ELI5:** a **saved playbook** Claude pulls off the shelf for a specific job — packaged instructions (plus optional scripts) invoked by name.

- **Claude Code:** a skill is a folder with a `SKILL.md`, in `.claude/skills/<name>/` (project) or `~/.claude/skills/` (personal), or delivered via **plugins**. Invoked like `/skill-name`.
- **Claude.ai:** **Agent Skills** exist as an Anthropic feature too. 🔎 confirm current availability/management in the firm's plan.
- **Why it matters:** skills make good workflows *repeatable and consistent* across a team — the org-level version of "save your best prompt."

---

## 6. How this maps in an enterprise environment (the firm's reality)
- **Admin console is the control room.** User provisioning, retention, connectors, data settings, and (for Code) managed policy all live with **admins**. 🔎 You/they must look here for the *actual* configured behavior before you teach specifics.
- **Data handling:** business data in Claude Enterprise is governed by the enterprise agreement (generally **not used to train models**) — 🔎 **confirm the current terms in their console**; don't state it from memory in a paid session.
- **What "markdown for Claude" means at the org level:** for the *web* product it's **Project custom instructions + uploaded knowledge** (managed in-app), not files on disk. For any **Claude Code** users, it's the `CLAUDE.md` hierarchy in §3, optionally with an IT-deployed managed file.
- **Your honest framing to leadership:** "Most of your 300 people need Projects, custom instructions, and good habits. MCP/skills/CLAUDE.md are for your technical users — powerful, but they need governance before you turn them loose."

---

## 7. What you MUST know vs. what you can skip (for now)
**Must know (you'll get asked):** the Code-vs-Enterprise distinction (§0), model/surface selection (§1), Projects-as-personas (§2), the data-training answer (§6), the stranger test + verify habit.
**Nice to know:** the full `CLAUDE.md` hierarchy (§3), skills mechanics (§5).
**Can skip until needed:** writing your own MCP servers, plugin authoring, subagent internals. Know they *exist* and what they're *for* — that's enough to sound credible and say "I can set that up / find out."

## 8. Your verify-before-you-teach list (do this before any paid session)
- [ ] 🔎 Current Claude model lineup + what the firm has access to (in-product)
- [ ] 🔎 The firm's Project availability, retention period, and data-training terms (admin console)
- [ ] 🔎 Which connectors/integrations are enabled for them
- [ ] 🔎 Whether they have Claude Code / Cowork at all, and for whom
- [ ] 🔎 Exact `CLAUDE.md` import syntax + managed-policy paths (official docs) if asked

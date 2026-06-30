# Changelog — 2026-06-30

## Session: Stand up the AI Enablement & Governance venture repo + first content

### Title
Initialized the project, defined positioning, and produced the first wave of teaching/governance/content artifacts for a non-technical-business AI enablement venture.

### Error / Issue
1. **No git repo existed** — the working directory (`C:\Users\aznkr\documents`) is the home Documents folder, not a project, so the required worktree-isolation workflow had nothing to branch from.
2. **Folder rename broke the worktree** — after renaming the project folder (`ai-enablement` → `AI_Enablement`), the linked git worktree pointed at the old absolute path and showed as `prunable`.
3. **Rename was blocked** — an earlier attempted rename failed with "Device or resource busy" / "used by another process."

### Root Cause
1. Expected — a brand-new venture had no repo yet.
2. Git worktrees store **absolute paths** in their `.git` link files; renaming a parent folder invalidates them.
3. A GUI program (File Explorer window and/or VS Code) held an open handle on the folder. (Ruled out git fsmonitor — not configured.)

### Fix
1. Created a dedicated project folder so git never tracks all of Documents, initialized it, and created an isolated session worktree:
```bash
mkdir -p AI_Enablement/docs && cd AI_Enablement
git init -b main
git worktree add -b session/<timestamp>-syllabus .claude/worktrees/claude-<timestamp>
```
2. Repaired the moved worktree by giving repair the NEW path explicitly, then pruned the stale entry:
```bash
git -C <main> worktree repair <new-worktree-path>
git -C <main> worktree prune
```
3. User closed the locking program; rename then succeeded.

### Education
- **Worktrees + renames:** never rename a repo/worktree parent folder casually — fix links afterward with `git worktree repair <new-path>`. The explicit path matters when the worktree itself moved (not just the main repo).
- **Two different Claude products:** Claude.ai **Enterprise** (web/Cowork) uses **Projects + custom instructions + connectors**; Claude **Code** (CLI) uses **`CLAUDE.md` + MCP + skills**. Teaching audiences must not blend them.
- **`CLAUDE.md` hierarchy:** managed (org) > user/global (`~/.claude/CLAUDE.md`) > project (committed) > subdirectory; settings split across `settings.json` / `settings.local.json`.
- **Remotion** = React-based programmatic video; several MCP servers bridge Claude → Remotion.

### Best Practices
- Keep a venture repo isolated in its own folder; never `git init` a home directory.
- Mark every version-specific product claim (model names, enterprise data terms, paths) as **verify-before-teach** — don't state them from memory in paid work.
- One idea per content asset; rule of 3; demo before theory; analogy first.

### Notes — what was built this session
- Positioning: AI **Enablement/Literacy** + **Governance**, sold as a bundle.
- Syllabus Tiers 0–5; full drafts of **Tier 1.5** (saving/organizing AI work, non-git audiences) and **Tier 5** (AI-enabled threats & defense).
- `docs/content-production-toolkit.md` (Remotion + infographics) and `docs/examples/` (Route A HTML infographic + Route B Figma spec, "LLM misuse" pain point).
- `docs/acceptable-use-policy-template.md` (fill-in-the-blanks AUP, Tier 3).
- `docs/ai-101/` (master outline, 6 lesson plans, video script, Q&A) and `docs/presenter/` (speaking best-practices + technical knowledge base).
- Git: 7 commits on `session/2026-06-29-232035-syllabus`; GitHub remote created and first PR opened this session.

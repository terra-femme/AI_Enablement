# AI Enablement & Governance

Educational content, playbooks, and governance templates for helping non-technical
organizations adopt AI/LLMs safely and effectively.

## What this is
A teaching + light-consulting venture covering two adjacent disciplines:
- **AI Enablement / Literacy** — helping everyone use AI well (training, playbooks, prompt libraries)
- **AI Governance** — the rules, data-handling, risk, and accountability layer (acceptable-use policy, data classification, human-in-the-loop)

## Syllabus (tiered — deliver in order)
- **Tier 0 — Foundations / Myth-busting**: cutoff vs. live, not-a-search-engine, what a model is, tokens & context, "does it train on our data?"
- **Tier 1 — Practical use**: model/surface selection, prompting basics, the verification habit, what never to paste in
- **Tier 1.5 — Saving, organizing & finding your AI work** (non-technical teams): no git/GitHub — Claude Projects + chat history for work-in-progress, cloud-drive Version History as the "save button," a team prompt library; bridges to governance (see `docs/tier1_5-saving-organizing-ai-work.md`)
- **Tier 2 — Role-based playbooks**: sales, HR, finance/ops, legal/compliance, exec
- **Tier 3 — Governance & safety**: acceptable-use policy, data classification, human-in-the-loop, shadow AI, NIST AI RMF / ISO 42001 awareness
- **Tier 4 — Rollout & measurement**: champions, adoption metrics, ROI, 30/60/90 plan
- **Tier 5 — AI-Enabled Threats & Defense**: how scammers use AI against businesses — AI-generated job applications & fake/deepfake candidates, AI phishing & Business Email Compromise, voice/video deepfakes, data leakage & shadow AI as attack surface, and a small-business defense playbook (see `docs/tier5-ai-threats.md`)

## Creator tooling (how to MAKE the content)
- `docs/content-production-toolkit.md` — Remotion (React-based video) MCP options, infographic routes (Claude Artifacts vs. Figma MCP), and the reusable infographic brief. This is the creator's workflow, not client-facing material.

## Repo layout
- `docs/` — drafts, skill outputs, changelogs, finished artifacts

## Built so far
- Syllabus Tiers 0–5 (Tier 1.5 + Tier 5 fully drafted in `docs/`)
- `docs/content-production-toolkit.md` — video (Remotion) + infographic workflow
- `docs/examples/` — Route A (HTML infographic) + Route B (Figma spec), LLM-misuse pain point
- `docs/acceptable-use-policy-template.md` — fill-in-the-blanks AI AUP (Tier 3)
- `docs/ai-101/` — full lunch & learn: master outline, 6 lesson plans, video script, Q&A cheat sheet
- `docs/presenter/` — presenter best-practices (speaking + advice-giving) + a technical knowledge base (MCPs, skills, CLAUDE.md hierarchy, Code-vs-Enterprise, personas)
- `docs/cheat-sheets/claude-power-cheat-sheet.md` — condensed end-user reference: CREF prompting, priming, result intention, Project contents, retrieval, connectors/MCPs, skills

## Next planned
- Tier 0 myth-busting scripts
- Tier 2 role-based playbook (HR or finance)
- Leave-behind 1-pager ("your 3 habits") as a Route A graphic

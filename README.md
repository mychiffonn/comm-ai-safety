# comm-ai-safety: Communicate AI safety research with evidence-preserving agent skills

`comm-ai-safety` is a portable bundle of Agent Skills for publishing AI-safety research accurately across public, press, and explanatory formats.

## Why this exists

AI-safety results are easy to overstate when they leave a paper. An elicited capability can be reported as typical model behavior; a benchmark score as real-world harm; or a model-only result as evidence of human misuse uplift. Each changes the claim.

The package gives researchers, communications teams, and independent explainers a fast, evidence-preserving workflow:

1. **Frame:** name one audience, one format, one communication goal, and the time available. Infer sensible defaults and state them instead of blocking on a long intake.
2. **Draft:** lead with one takeaway and at most two supporting points. Attach a source, an interpretation-changing condition, and a boundary to each, then deliver a clearly labeled working draft.
3. **Verify:** check every load-bearing claim, number, headline, caption, and quote against the primary sources. Expand to a full claim ledger only for high-risk, contested, or deep-dive work.
4. **Approve:** before publication, have a responsible human approve the core evidence map, test the revised draft with a representative reader, and run the proportionate audit.

The first draft is an early deliverable, not a publication gate. Human approval and reader testing happen on concrete copy, where they can catch both scientific errors and misleading simplification.

This is a quality-control layer for communication, not a substitute for subject-matter, security, legal, or editorial review. Its intended effect is concrete: readers can distinguish **capability**, **propensity**, **misuse uplift**, and **observed deployment evidence**, rather than treating them as interchangeable.

## What is included

| Skill         | Use it to                                                                                        | Key safeguard                                                                                            |
| ------------- | ------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------- |
| `comm-public` | Create explainers, FAQs, social copy, visual briefs, and safer demo briefs from primary sources. | One-message rapid brief, core evidence map, comprehension check, and demo safety gate.                    |
| `comm-press`  | Create releases, media briefs, pitches, and journalist FAQs.                                     | Fast working draft, source-verifiable core claims, independent context, quote approval, and final audit. |
| `comm-audit`  | Check a public artifact or coverage corpus against authoritative sources.                        | Rapid core-claim check or full claim-to-source audit, scaled to publication risk.                        |

The authoring skills deliberately separate the audience artifact from the process record. They save the requested `<short-paper-name>.<extension>` while keeping evidence cards, verification queues, and approval notes in the chat or harness unless the user asks to persist them or the run is a repository demo. `comm-audit` can provide a rapid, non-readiness check during drafting and a full publication or corpus audit when the stakes, contestation, or reuse justify it.

The skills are informed by evidence on public-engagement barriers, audience-centred communication, uncertainty communication, AI evaluation practice, press-release exaggeration, and AI journalism pitfalls. Their operational sources are linked in each skill’s `references/` directory.

## Skills

```text
skills/
├── comm-audit/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   ├── references/audit-criteria.md
│   └── assets/audit-report-template.md
├── comm-public/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   ├── references/
│   │   ├── public-formats-and-demos.md
│   │   └── researcher-social-formats.md
│   └── assets/
│       ├── demo-brief-template.md
│       ├── public-draft-template.md
│       └── public-package-template.md
└── comm-press/
    ├── SKILL.md
    ├── agents/openai.yaml
    ├── references/press-principles-and-pitfalls.md
    └── assets/
        ├── press-draft-template.md
        └── press-package-template.md
```

### `comm-audit`

Audits a single artifact or a corpus against authoritative technical sources. It applies one coding frame to claims, conditions, quantitative context, caveats, anthropomorphism, independence, related work, rights, safety, accessibility, and communication quality. It also records strong language and structure worth retaining instead of rewarding blandness.

Example prompts:

```text
Use $comm-audit to review this explainer against the paper and supplement.

Use $comm-audit to compare all articles in this coverage inventory with one claim ledger.
```

### `comm-public`

Creates plain-language summaries, explainers, FAQs, visuals, X/Twitter threads, researcher-facing LessWrong/Alignment Forum posts, and safe demo briefs or websites. It treats interactive demos as replication, illustration, simulation, or live behavior and applies an explicit dual-use and accessibility gate.

It saves the audience artifact as `<short-paper-name>.<requested-extension>`, defaulting to Markdown. Briefs, evidence, and workflow notes normally stay in chat; `comm-public-run.md` is retained only for demos or explicit requests.

Example prompts:

```text
Use $comm-public to turn this paper and supplement into a layered public explainer.

Use $comm-public to check my understanding of this evaluation, then help me make an accessible results explorer.
```

### `comm-press`

Creates university/lab news releases, media briefs, pitches, journalist FAQs, and press packages, then invokes `comm-audit`. It includes the 18 AI-journalism pitfalls identified by Sayash Kapoor and Arvind Narayanan, independent-context checks, quote approval, rights tracking, and target-distributor policy checks.

It saves the audience artifact as `<short-paper-name>.<requested-extension>`, defaulting to Markdown. Briefs, evidence, and workflow notes normally stay in chat; `comm-press-run.md` is retained only for demos or explicit requests.

Example prompts:

```text
Use $comm-press to prepare a university news release and media brief for this preprint.

Use $comm-audit to audit this lab announcement for hype, missing conditions, and unsupported misuse claims.
```

## Install

From the terminal:

```bash
npx skills add mychiffonn/comm-ai-safety
```

`comm-public` and `comm-press` can be installed alone for drafting, but their workflows must not label work audited, final, or publishable unless `comm-audit` is available and run.

## Project pitch

The short project overview is available as [Markdown](outputs/comm-ai-safety-pitch.md), [PDF](outputs/comm-ai-safety-pitch.pdf), and [PowerPoint](outputs/comm-ai-safety-pitch.pptx).

## Demo

[`demo/emergent-misalignment/`](demo/emergent-misalignment/) applies the workflows to the 2025 ICML and expanded 2026 Nature versions of the Emergent Misalignment research. Its `comm-press` run uses the Nature article to produce a 30-second overview, three takeaways, and a standalone public-facing [`emergent-misalignment.md`](demo/emergent-misalignment/emergent-misalignment.md). The broader demo also contains an indexed-public-web coverage inventory, comparative `comm-audit` report, and writing patterns learned from press, researcher X threads, and LessWrong/Alignment Forum posts.

Review skill instructions before installing them; skills operate with the permissions of the agent that runs them.

## Contribute

Contributions should improve source fidelity, audience usefulness, or workflow safety without adding unnecessary context.

1. Open an issue or proposal describing the communication failure mode and a realistic prompt/source example.
2. Keep the core workflow in `SKILL.md`; put detailed, selectively loaded guidance in `references/` and reusable output scaffolds in `assets/`.
3. Use primary or authoritative sources where possible. Add a direct link and state the operational rule the source supports; distinguish professional guidance from empirical evidence and drafts from final standards.
4. Preserve the pre-publication human approval gate and the capability/propensity/misuse-uplift distinctions. Do not turn approval into a pre-draft bottleneck.
5. Update `comm-audit` when adding a cross-channel audit requirement; keep channel-specific drafting checks in the relevant authoring skill.
6. Validate all affected skill folders and run `npx skills add . --list` before submitting changes.
7. In the contribution, include a forward-test prompt and the resulting artifact or traceability/audit excerpt. Do not include confidential, embargoed, personal, or operationally hazardous material.

When proposing a new audience skill, keep its authoring guidance self-contained and make any dependency on `comm-audit` explicit in its workflow and installation example.

## Scope and responsibility

These skills support communication and review; they do not replace subject-matter, security, legal, licensing, accessibility, or publication-platform review. An artifact is not publishable until the skill's human gates and material audit items are resolved.

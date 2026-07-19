# comm-ai-safety: Communicate AI safety research with evidence-preserving agent skills

`comm-ai-safety` is a portable bundle of Agent Skills for publishing AI-safety research accurately across public, press, and explanatory formats.

## Why this exists

AI-safety results are easy to overstate when they leave a paper. An elicited capability can be reported as typical model behavior; a benchmark score as real-world harm; or a model-only result as evidence of human misuse uplift. Each changes the claim.

The package gives researchers, communications teams, and independent explainers a repeatable publication workflow:

1. Extract a source-anchored claim ledger: result, conditions, numbers, scope, and caveats.
2. Have a responsible human approve the claims and a representative reader test their understanding.
3. Adapt the approved claims for one audience and format.
4. Audit the finished artifact against the sources before calling it audited or publishable.

This is a quality-control layer for communication, not a substitute for subject-matter, security, legal, or editorial review. Its intended effect is concrete: readers can distinguish **capability**, **propensity**, **misuse uplift**, and **observed deployment evidence**, rather than treating them as interchangeable.

## What is included

| Skill | Use it to | Key safeguard |
|---|---|---|
| `comm-public` | Create explainers, FAQs, social copy, visual briefs, and safer demo briefs from primary sources. | Audience brief, claim ledger, comprehension check, and demo safety gate. |
| `comm-press` | Create releases, media briefs, pitches, and journalist FAQs. | Source-verifiable claims, independent context, quote approval, and final audit. |
| `comm-audit` | Check a public artifact or coverage corpus against authoritative sources. | Claim-to-source matrix plus findings on conditions, caveats, numbers, safety, rights, and accessibility. |

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
│       └── public-package-template.md
└── comm-press/
    ├── SKILL.md
    ├── agents/openai.yaml
    ├── references/press-principles-and-pitfalls.md
    └── assets/
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

Example prompts:

```text
Use $comm-public to turn this paper and supplement into a layered public explainer.

Use $comm-public to check my understanding of this evaluation, then help me make an accessible results explorer.
```

### `comm-press`

Creates university/lab news releases, media briefs, pitches, journalist FAQs, and press packages, then invokes `comm-audit`. It includes the 18 AI-journalism pitfalls identified by Sayash Kapoor and Arvind Narayanan, independent-context checks, quote approval, rights tracking, and target-distributor policy checks.

Example prompts:

```text
Use $comm-press to prepare a university news release and media brief for this preprint.

Use $comm-audit to audit this lab announcement for hype, missing conditions, and unsupported misuse claims.
```

## Install

The repository follows the open Agent Skills layout: every installable skill is a folder under `skills/` with a valid `SKILL.md` containing `name` and `description` frontmatter.

From a local clone, list the skills:

```bash
npx skills add . --list
```

Install the bundle interactively:

```bash
npx skills add .
```

Install an authoring skill with its audit dependency for Codex:

```bash
npx skills add . --skill comm-audit --skill comm-public --agent codex
npx skills add . --skill comm-audit --skill comm-press --agent codex
```

Install only the standalone auditor:

```bash
npx skills add . --skill comm-audit --agent codex
```

After the repository is published, replace `.` with its GitHub shorthand or URL, for example:

```bash
npx skills add mychiffonn/comm-ai-safety --skill comm-audit --skill comm-public
```

`comm-public` and `comm-press` can be installed alone for drafting, but their workflows must not label work audited, final, or publishable unless `comm-audit` is available and run.

## Demo

[`demo/emergent-misalignment/`](demo/emergent-misalignment/) applies the workflows to the 2025 ICML and expanded 2026 Nature versions of the Emergent Misalignment research. It contains a versioned claim ledger awaiting human approval, an indexed-public-web coverage inventory, a comparative `comm-audit` report, and writing patterns learned from press, researcher X threads, and LessWrong/Alignment Forum posts.

Review skill instructions before installing them; skills operate with the permissions of the agent that runs them.

## Contribute

Contributions should improve source fidelity, audience usefulness, or workflow safety without adding unnecessary context.

1. Open an issue or proposal describing the communication failure mode and a realistic prompt/source example.
2. Keep the core workflow in `SKILL.md`; put detailed, selectively loaded guidance in `references/` and reusable output scaffolds in `assets/`.
3. Use primary or authoritative sources where possible. Add a direct link and state the operational rule the source supports; distinguish professional guidance from empirical evidence and drafts from final standards.
4. Preserve the mandatory main-claim human checkpoint and the capability/propensity/misuse-uplift distinctions.
5. Update `comm-audit` when adding a cross-channel audit requirement; keep channel-specific drafting checks in the relevant authoring skill.
6. Validate all affected skill folders and run `npx skills add . --list` before submitting changes.
7. In the contribution, include a forward-test prompt and the resulting artifact or traceability/audit excerpt. Do not include confidential, embargoed, personal, or operationally hazardous material.

When proposing a new audience skill, keep its authoring guidance self-contained and make any dependency on `comm-audit` explicit in its workflow and installation example.

## Scope and responsibility

These skills support communication and review; they do not replace subject-matter, security, legal, licensing, accessibility, or publication-platform review. An artifact is not publishable until the skill's human gates and material audit items are resolved.

# comm-ai-safety: Communicate AI safety research with evidence-preserving agent skills

`comm-ai-safety` is a portable bundle of Agent Skills for turning technical AI safety sources into public communication without dropping the conditions, uncertainty, caveats, and provenance that determine what a result actually means.

It supports two complementary users:

- researchers creating a reviewable public communication package around their own work;
- non-researchers learning from primary technical sources and producing an audience-appropriate explainer, release, or supporting artifact.

## Motivation and theory of change

Public-facing research communication is valuable but structurally difficult. Research on public engagement reports limited time, resources, training, institutional support, and career recognition ([recent UK survey](https://pmc.ncbi.nlm.nih.gov/articles/PMC12972233/); [review of public-engagement literature](https://pmc.ncbi.nlm.nih.gov/articles/PMC8263305/)). At the same time, simply adding more facts is not enough: audiences bring different goals, knowledge, values, and trust relationships ([National Academies](https://www.nationalacademies.org/read/23674/chapter/4)). AI safety adds unusually sharp failure modes: elicited capability can be reported as ordinary behavior, model-only scores as human misuse uplift, and a benchmark as real-world harm.

| Communication bottleneck                     | Bundle response                                                               |
| -------------------------------------------- | ----------------------------------------------------------------------------- |
| Time, skill, and coordination cost           | Reusable workflows, checklists, and package templates                         |
| Fear of misstatement or hype                 | Claim ledger, source anchors, human approval, and adversarial audit           |
| Different audience needs                     | Explicit audience brief, detail budget, layering, and comprehension tests     |
| Evaluation nuance lost in translation        | Capability/propensity/misuse-uplift labels and condition-preserving language  |
| Demos create misunderstanding or misuse risk | Demo classification, threat review, disclosure, and accessibility gates       |
| Communication labor receives little credit   | Named contributor/reviewer roles, versioned packages, and suggested citations |

### The gap

AI-safety communication often fails at the exact point where evidence moves from a technical source to a decision-relevant public claim. A headline can turn an elicited capability into ordinary model behavior; a benchmark result into demonstrated real-world harm; or a model-only outcome into a claim about human misuse. These are not merely stylistic errors: they can distort public understanding, make it harder for journalists and decision-makers to evaluate evidence, and create avoidable hype or panic around safety research.

Existing writing guidance rarely gives a researcher, communications professional, or independent explainer a reusable way to preserve **provenance, evaluation conditions, uncertainty, and scope** across a release, explainer, social post, visual, and demo. This package fills that operational gap.

### Who it is for

- **AI-safety researchers and research leads** who need a reviewable way to communicate their work without overclaiming it.
- **University and lab communications teams** who need newsworthy, source-verifiable press materials under time pressure.
- **Journalists, independent explainers, and technically curious community members** who need to translate primary sources for a specific audience while retaining the details that change a claim’s meaning.

### How it creates value

The intervention is intentionally narrow: make accurate communication the easier default at the moment people draft and review public-facing material.

1. A user starts with primary sources and creates a compact, source-anchored claim ledger.
2. A responsible human validates the main claims and a representative reader checks their understanding.
3. The authoring skills adapt those approved claims to a defined audience and format without separating them from material conditions and caveats.
4. `comm-audit` independently checks the finished artifact against the ledger and source record, flagging claim inflation, missing context, unsafe demo design, rights issues, and accessibility gaps before publication.
5. The resulting package leaves behind reusable evidence, reviewer roles, and an audit trail that can be updated, credited, and reused across channels.

If teams adopt this workflow, fewer public artifacts should collapse capability, propensity, misuse uplift, and observed deployment evidence into one another. That gives readers and decision-makers more trustworthy information to scrutinize, while reducing the time and coordination burden that otherwise discourages careful outreach. The package does **not** claim that better communication alone changes institutional incentives, policy, or model behavior; its contribution is a practical quality-control layer at a known failure point.

This bundle reduces the work needed to produce reusable communication artifacts while keeping humans responsible for the main claims. The authoring skills use the same backbone:

1. inventory the authoritative sources;
2. extract a traceable main-claim ledger;
3. pause for human validation or teach-back;
4. choose an audience and explicit detail budget;
5. draft a layered package;
6. invoke `comm-audit` to check claims, numbers, conditions, caveats, language, context, rights, safety, and accessibility.

The bundle can lower marginal effort and make communication work easier to review, reuse, and credit. It cannot by itself change promotion, funding, or publication incentives; institutions still need to recognize this work.

The workflow is informed by evidence on barriers to public engagement, audience-centered science communication, plain-language summaries, uncertainty communication, AI evaluation practice, press-release exaggeration, and AI journalism pitfalls. The source links and their operational implications live in each skill's `references/` directory.

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

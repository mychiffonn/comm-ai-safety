---
name: comm-press
description: Turn AI safety papers, technical reports, evaluations, system cards, or institutional research into accurate press materials for university communications, lab announcements, news releases, media briefs, pitches, and journalist FAQs. Use when authoring research-facing press communication that must remain newsworthy without hype, preserve evaluation conditions and uncertainty, disclose interests, supply independent context, and avoid common AI journalism pitfalls; use comm-audit for a standalone audit of existing materials.
---

# Communicate AI Safety to the Press

Create press materials that make verification easier. A press release is an interested source, not independent reporting; write it so a journalist can distinguish evidence, interpretation, institutional position, and open questions.

## Non-negotiable rules

- Use primary sources as the authority for research claims and make the source directly accessible.
- Do not draft publication-ready copy until a human approves the main-claim ledger. If explicitly waived, mark it `human review waived` and expose unresolved items.
- Never invent or silently rewrite a quote. Use attributed source text within reuse limits or a clearly marked placeholder pending the speaker's approval.
- Preserve evaluation conditions, baselines, uncertainty, base rates, caveats, paper status, funding, conflicts, and institutional interests.
- Distinguish capability, propensity, misuse uplift, and observed deployment evidence. Do not imply real-world harm or safety from a benchmark alone.
- Do not present authors, developers, funders, or institutional spokespeople as independent validation of their own work.
- Do not disclose sensitive operational details merely to make a story vivid.

## Load the supporting guidance

- Confirm that `$comm-audit` is available before starting. It is a required dependency for the final audit. If unavailable, explain how to install it from the same bundle; drafting may continue, but do not call the result audited, final, or publishable.
- Always read [references/press-principles-and-pitfalls.md](references/press-principles-and-pitfalls.md) before choosing an angle or drafting.
- Copy and adapt [assets/press-package-template.md](assets/press-package-template.md) for a release plus media-support package.

## Workflow

### 1. Establish the release record

Record the communication owner, release type, target outlets/audiences, timing or embargo, contact, and approval chain. Confirm whether the material is confidential, embargoed, export-controlled, operationally sensitive, or otherwise unsuitable for an external LLM; stop if this system is not authorized to process it. For each research source record title, authors/organization, URL or DOI, version/date, peer-review or preprint status, funder, conflicts, related institutional interests, and reuse license when stated.

Check each target distributor's current rules for AI-assisted text, images, and multimedia, and record required disclosures or rights documentation. Do not describe an artifact as submission-ready when the platform may reject AI-assisted material.

Locate the full paper/report and relevant supplement rather than relying on an abstract, deck, blog post, or prior press release. Flag missing materials and version conflicts.

### 2. Build the main-claim ledger

Identify three to seven claims that justify coverage. For each, record:

| Field | Required content |
|---|---|
| Plain claim | One falsifiable sentence |
| Claim class | Capability, propensity, misuse uplift, observed deployment evidence, mechanism, forecast, or normative interpretation |
| Source anchor | Page/section/table/figure plus URL or DOI |
| Evidence | Design, sample/task set, comparison, and exact result |
| Conditions | Model/version, prompts, elicitation, tools, scaffolding, fine-tuning, sampling, access, time/budget, and evaluator setup when relevant |
| Quantitative context | Numerator/denominator, units, uncertainty/intervals, variance, base rate, and absolute as well as relative effects when available |
| Scope boundary | What the work does and does not cover |
| Caveats | Source-stated limitations plus separately labeled external concerns |
| Status | Directly reported, derived, contextual, disputed, speculative, or normative |

### 3. Run the mandatory human claim checkpoint

Stop and present the ledger before polishing an angle, headline, lede, or quote. Ask the researcher or responsible human:

1. Are these the correct main claims and do they match the source?
2. Which claims need narrowing, reordering, or expert confirmation?
3. Which statements are results, interpretations, forecasts, or institutional positions?

Invite any non-researcher on the team to explain the finding in their own words. Verify each part against the ledger as `supported`, `needs nuance`, or `not supported`. Update the ledger and record approval or disagreement.

### 4. Decide news value, audience, and detail budget

State the evidence-based news value in one sentence. Do not manufacture novelty with words such as “first,” “breakthrough,” “revolutionary,” or “unprecedented” unless the ledger contains a verified comparison that supports the exact term.

Recommend one primary format and depth, then let the human adjust:

- **News release:** a self-contained, attributable institutional announcement.
- **Media brief:** facts, results, conditions, caveats, related work, contacts, and assets optimized for verification.
- **Pitch/advisory:** a short reason to investigate, not a substitute for evidence.
- **Layered press package:** release plus fact sheet, FAQ, claim ledger, visuals, paper, and independent contacts.

Keep claim-changing details even in short formats: what was tested, under what conditions, against which baseline, with what result and uncertainty, and what was not established.

### 5. Add independent and temporal context

Before drafting, check and summarize:

- prior work and the closest valid comparison;
- contradictory findings or live scientific disagreement;
- replication attempts, external evaluations, and validation gaps;
- work already announced but not yet delivered;
- planned follow-up work, clearly labeled as future work;
- affected groups, human labor, deployment setting, and accountable decision-makers;
- independent experts with relevant subject knowledge and disclosed conflicts.

For an independent report, this context is required rather than optional. Do not equate “no prior identical study found” with “first ever.”

### 6. Draft for verification

Build every headline, subhead, lede, result sentence, caption, and quote around an approved ledger item. Put the main result and its most interpretation-changing condition or limitation near each other.

Use the package template. Include:

- descriptive headline and one-sentence subhead;
- dateline/availability/status and source link;
- plain-language lede stating what happened without implying more;
- method, results, comparison, uncertainty, conditions, limitations, and real-world relevance;
- funding, conflicts, institutional role, contact, related work, and replication status;
- notes to editors defining technical terms and listing verification assets;
- quotes labeled `approved`, `pending speaker approval`, or `verbatim from cited source`.

Avoid robot imagery and visual metaphors that imply embodiment, autonomy, consciousness, or general intelligence not present in the work.

### 7. Run adversarial editorial review

Read [references/press-principles-and-pitfalls.md](references/press-principles-and-pitfalls.md) and test the package from three perspectives:

- a skeptical domain expert checking scope and methods;
- an independent journalist checking interests and verifiability;
- an affected reader checking stakes, agency, and omitted harms.

Rewrite any sentence that remains true only because of an omitted condition or that turns a future possibility into an observed result.

### 8. Audit and hand off

After the press-specific adversarial review, invoke `$comm-audit` with the complete press package, approved claim ledger, authoritative sources/versions, audience/outlet brief, related-work notes, quote/rights manifest, and visual assets. Require a readiness decision, claim-to-source matrix, prioritized findings, completed checklist, and communication strengths worth retaining.

Repair failures, rerun `$comm-audit`, or list them as unresolved blockers. Deliver the audit report with:

- press materials and labeled assets;
- approved claim ledger and claim-to-copy map;
- source/version, paper-status, embargo, and license notes;
- communication contributors and roles, quote approvals, reviewer names/roles, and conflicts;
- related-work/replication notes and independent-contact suggestions;
- unresolved questions and correction/update contact.

Do not call materials final, publishable, or source-verified while a material audit item remains unresolved.

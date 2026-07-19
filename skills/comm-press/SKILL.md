---
name: comm-press
description: Turn AI safety papers, technical reports, evaluations, system cards, or institutional research into accurate press materials saved with a short paper name and the requested extension, defaulting to Markdown, while presenting evidence and workflow notes in the chat or harness. Use when authoring university communications, lab announcements, news releases, media briefs, pitches, journalist FAQs, or other research-facing press communication that must remain newsworthy without hype, preserve evaluation conditions and uncertainty, disclose interests, supply independent context, and avoid common AI journalism pitfalls; use comm-audit for a standalone audit of existing materials.
---

# Communicate AI Safety to the Press

Create press materials that make verification easier. A press release is an interested source, not independent reporting; write it so a journalist can distinguish evidence, interpretation, institutional position, and open questions.

## Non-negotiable rules

- Use primary sources as the authority for research claims and make the source directly accessible.
- Draft early, but label unapproved copy `working draft — not yet verified or approved`. Do not call copy final, publishable, or source-verified until a responsible human approves the core evidence map and material audit findings are resolved.
- Never invent or silently rewrite a quote. Use attributed source text within reuse limits or a clearly marked placeholder pending the speaker's approval.
- Preserve evaluation conditions, baselines, uncertainty, base rates, caveats, paper status, funding, conflicts, and institutional interests.
- Distinguish capability, propensity, misuse uplift, and observed deployment evidence. Do not imply real-world harm or safety from a benchmark alone.
- Do not present authors, developers, funders, or institutional spokespeople as independent validation of their own work.
- Do not disclose sensitive operational details merely to make a story vivid.

## Load the supporting guidance

- Confirm that `$comm-audit` is available before starting. It is a required dependency for the final audit. If unavailable, explain how to install it from the same bundle; drafting may continue, but do not call the result audited, final, or publishable.
- Always read [references/press-principles-and-pitfalls.md](references/press-principles-and-pitfalls.md) before choosing an angle or drafting.
- Copy and adapt [assets/press-draft-template.md](assets/press-draft-template.md) for the audience-facing draft.
- Copy and adapt [assets/press-package-template.md](assets/press-package-template.md) for the internal run record and later media-support package.

## Interface and artifact contract

Choose a short, recognizable, lowercase hyphenated paper name, normally two to six words; honor a user-supplied name. Use the extension the user requests. If none is requested, use `.md`.

For an ordinary run:

- Save only the audience-facing artifact as `<short-paper-name>.<extension>` in the user-selected output directory, or the current task directory when no output directory is specified.
- Present the rapid brief, core evidence map, verification queue, approval state, and other process output in the AI chat or harness interface. Do not create `comm-press-run.md` unless the user asks to persist the run.
- Keep evidence tables, verification queues, approval checklists, and agent workflow notes out of the audience artifact.

For a repository demo:

- Write the audience artifact to `demo/<short-paper-name>/<short-paper-name>.<extension>`.
- Write the interface output to `demo/<short-paper-name>/comm-press-run.md` so the demo shows what the tool presented. Link to the audience artifact; do not duplicate its full text.

For non-Markdown output, use the relevant document, PDF, or presentation workflow and verify the rendered artifact. Do not leave an extra Markdown copy unless the user requests both formats.

## Workflow

### 1. Set the rapid press brief

Identify the primary source and state one target reader, one press format, the news question, tone, length, and deadline. Infer missing choices and label them; ask only when confidentiality, embargo, safety, or a materially different editorial direction requires an answer. Confirm whether the material is confidential, embargoed, export-controlled, operationally sensitive, or otherwise unsuitable for an external LLM; stop if this system is not authorized to process it.

Locate the full paper/report and relevant supplement rather than relying on an abstract, deck, blog post, or prior press release. Record source version/status and flag missing materials or version conflicts.

### 2. Make a three-point message map and draft

Read the abstract/executive summary, conclusion/discussion, and the central result, table, or figure. Choose one main takeaway and at most two supporting claims. Also state why it matters to this press audience and the leading limitation or non-finding.

Create one compact evidence card per core claim:

| Field | Required content |
|---|---|
| Plain claim | One falsifiable sentence |
| Claim class | Capability, propensity, misuse uplift, observed deployment evidence, mechanism, forecast, or normative interpretation |
| Source anchor | Page/section/table/figure plus URL or DOI |
| Evidence | Central design/result and comparison |
| Conditions | Only conditions that change how the claim should be interpreted |
| Number context | Denominator/unit, baseline, uncertainty, and selection status when material |
| Boundary | The most likely overreading and what the work does not establish |
| Status | Directly reported, derived, contextual, disputed, speculative, or normative |

Immediately deliver:

1. a 30-second press brief: `what happened / why it matters / what not to conclude`;
2. `<short-paper-name>.<extension>` containing the working headline, lede, and requested audience-facing draft;
3. in the chat or harness, the evidence cards and a short `verify next` list. Persist this interface output to `comm-press-run.md` only for a demo or when explicitly requested.

Use `[VERIFY]`, `[SOURCE NEEDED]`, and `[QUOTE PENDING]` instead of guessing. Make the provisional status visible.

### 3. Verify and redraft

Check the headline, lede, one to three core claims, every material number, comparison, caption, quote, and paper-status statement in the audience artifact against primary sources. Update the evidence record in the chat or harness, and in `comm-press-run.md` when running a demo. Add the closest prior work, contradictory results, replications/challenges, funding/conflicts, institutional interests, rights, and current distributor rules that matter to the proposed package. Record required AI-assistance disclosures or rights documentation; do not describe an artifact as submission-ready when the platform may reject it.

Expand to a full ledger of conditions, quantitative context, caveats, and scope only for high-stakes, contested, long-form, or multi-channel work. Revise the copy so each interpretation-changing condition or limitation sits beside the claim it changes.

### 4. Get human approval on the revised draft

Present the revised draft and core evidence map together. Ask the researcher or responsible human:

1. Are these the correct main claims and do they match the source?
2. Which claims need narrowing, reordering, or expert confirmation?
3. Which statements are results, interpretations, forecasts, or institutional positions?

Record approval, required changes, and disagreements. Approval applies to the dated draft and sources. Representative-reader testing happens after the draft exists and checks comprehension, not scientific validity.

### 5. Set the final detail budget

State the evidence-based news value in one sentence. Do not manufacture novelty with words such as “first,” “breakthrough,” “revolutionary,” or “unprecedented” unless the evidence map contains a verified comparison that supports the exact term.

Recommend one primary format and depth, then let the human adjust:

- **News release:** a self-contained, attributable institutional announcement.
- **Media brief:** facts, results, conditions, caveats, related work, contacts, and assets optimized for verification.
- **Pitch/advisory:** a short reason to investigate, not a substitute for evidence.
- **Layered press package:** release plus fact sheet, FAQ, evidence map or expanded ledger, visuals, paper, and independent contacts.

Keep claim-changing details even in short formats: what was tested, under what conditions, against which baseline, with what result and uncertainty, and what was not established.

### 6. Add independent and temporal context

Before finalizing, check and summarize:

- prior work and the closest valid comparison;
- contradictory findings or live scientific disagreement;
- replication attempts, external evaluations, and validation gaps;
- work already announced but not yet delivered;
- planned follow-up work, clearly labeled as future work;
- affected groups, human labor, deployment setting, and accountable decision-makers;
- independent experts with relevant subject knowledge and disclosed conflicts.

For an independent report, this context is required rather than optional. Do not equate “no prior identical study found” with “first ever.”

### 7. Complete the press package

Build every headline, subhead, lede, result sentence, caption, and quote around an approved evidence-card or ledger item. Put the main result and its most interpretation-changing condition or limitation near each other.

Use the package template. Include:

- descriptive headline and one-sentence subhead;
- dateline/availability/status and source link;
- plain-language lede stating what happened without implying more;
- method, results, comparison, uncertainty, conditions, limitations, and real-world relevance;
- funding, conflicts, institutional role, contact, related work, and replication status;
- notes to editors defining technical terms and listing verification assets;
- quotes labeled `approved`, `pending speaker approval`, or `verbatim from cited source`.

Avoid robot imagery and visual metaphors that imply embodiment, autonomy, consciousness, or general intelligence not present in the work.

### 8. Run adversarial editorial review

Read [references/press-principles-and-pitfalls.md](references/press-principles-and-pitfalls.md) and test the package from three perspectives:

- a skeptical domain expert checking scope and methods;
- an independent journalist checking interests and verifiability;
- an affected reader checking stakes, agency, and omitted harms.

Rewrite any sentence that remains true only because of an omitted condition or that turns a future possibility into an observed result.

### 9. Audit and hand off

Use `$comm-audit` rapid mode on the working headline, lede, and core evidence map when early feedback is useful. Before publication, invoke its full mode with the complete press package, approved core evidence map or claim ledger, authoritative sources/versions, audience/outlet brief, related-work notes, quote/rights manifest, and visual assets.

Repair failures in the standalone draft, rerun `$comm-audit`, or list them as unresolved blockers. Deliver the audit report with:

- `<short-paper-name>.<extension>` and labeled assets;
- for demos or explicit persistence requests only, `comm-press-run.md` containing the evidence and workflow record;
- approved core evidence map or expanded claim ledger, plus a claim-to-copy map;
- source/version, paper-status, embargo, and license notes;
- communication contributors and roles, quote approvals, reviewer names/roles, and conflicts;
- related-work/replication notes and independent-contact suggestions;
- unresolved questions and correction/update contact.

Do not call materials final, publishable, or source-verified while a material audit item remains unresolved.

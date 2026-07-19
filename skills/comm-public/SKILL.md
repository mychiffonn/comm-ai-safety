---
name: comm-public
description: Turn AI safety papers, technical reports, evaluations, system cards, or other primary sources into grounded public communication saved with a short paper name and the requested extension, defaulting to Markdown, while presenting evidence and workflow notes in the chat or harness. Use when a researcher needs a public summary, explainer, FAQ, visual brief, social copy, or safe interactive website/demo, or when a non-researcher needs to understand and explain technical AI safety results without losing conditions, uncertainty, caveats, or provenance.
---

# Communicate AI Safety to the Public

Create accessible communication without making the underlying evidence sound stronger, broader, or more settled than it is. Give the user a useful working draft quickly, then verify and revise its load-bearing claims before publication.

## Non-negotiable rules

- Use primary sources as the authority for claims. Label secondary context, interpretation, and speculation separately.
- Draft early, but label unapproved copy `working draft — not yet verified or approved`. Do not call copy final, publishable, or source-verified until a responsible human approves the core evidence map and material audit findings are resolved.
- Preserve evaluation conditions, comparison baselines, uncertainty, base rates, caveats, paper status, and conflicts that could change interpretation.
- Distinguish capability, propensity, misuse uplift, and observed deployment evidence. Do not substitute one for another.
- Never invent a quote, citation, number, consensus, implication, or author intention.
- Prefer an explorable results demo over unrestricted model access. Do not expose hazardous prompts, operational instructions, private data, credentials, or a vulnerable endpoint.

## Load the supporting guidance

- Confirm that `$comm-audit` is available before starting. It is a required dependency for the final audit. If unavailable, explain how to install it from the same bundle; drafting may continue, but do not call the result audited, final, or publishable.
- Read [references/public-formats-and-demos.md](references/public-formats-and-demos.md) when selecting an audience, format, visual, or interactive demo.
- For X/Twitter, Bluesky, Mastodon, LessWrong, Alignment Forum, lab-blog, or similar researcher-facing outputs, also read [references/researcher-social-formats.md](references/researcher-social-formats.md).
- Copy and adapt [assets/public-draft-template.md](assets/public-draft-template.md) for the audience-facing draft.
- Copy and adapt [assets/public-package-template.md](assets/public-package-template.md) for the internal run record or a multi-part package.
- Copy and adapt [assets/demo-brief-template.md](assets/demo-brief-template.md) before building a website or interactive demo.

## Interface and artifact contract

Choose a short, recognizable, lowercase hyphenated paper name, normally two to six words; honor a user-supplied name. Use the extension the user requests. If none is requested, use `.md`.

For an ordinary run:

- Save only the audience-facing artifact as `<short-paper-name>.<extension>` in the user-selected output directory, or the current task directory when no output directory is specified.
- Present the audience brief, 30-second orientation, core evidence map, verification queue, approval state, and other process output in the AI chat or harness interface. Do not create `comm-public-run.md` unless the user asks to persist the run.
- Keep evidence tables, verification queues, approval checklists, and agent workflow notes out of the audience artifact.

For a repository demo:

- Write the audience artifact to `demo/<short-paper-name>/<short-paper-name>.<extension>`.
- Write the interface output to `demo/<short-paper-name>/comm-public-run.md` so the demo shows what the tool presented. Link to the audience artifact; do not duplicate its full text.

For non-Markdown output, use the relevant document, PDF, or presentation workflow and verify the rendered artifact. Do not leave an extra Markdown copy unless the user requests both formats.

## Workflow

### 1. Set a rapid delivery frame

Identify the primary source, then state a compact delivery frame: one audience, one communication goal, requested format/channel, tone, length, and deadline. Infer missing choices from the request and label the assumptions. Ask only when a missing choice would materially change the result; do not make the user complete an intake before seeing useful copy.

Before the first draft, record the primary source's title, URL or DOI, date/version, and publication status. Flag obvious version conflicts or missing central results. Complete the full source, funding/conflict, supplement, code/data, and rights record during verification.

State:

- who the single primary audience is and what they already know;
- what they care about, decide, or want to do next;
- likely misconceptions, without treating disagreement as ignorance;
- the tone, register, language, and reading context to use;
- channel, deadline, communication owner, and accessibility or language needs.

Recommend one primary audience rather than writing for "everyone." Do not assume the goal is persuasion: choose among informing, enabling a decision, inviting scrutiny, teaching a concept, gathering feedback, or motivating a clearly supported action.

### 2. Build a message map and deliver the first draft

Read the abstract or executive summary, conclusion/discussion, and the central result, table, or figure before drafting. Create a compact message map with:

- one obvious main takeaway in one or two sentences;
- up to two supporting claims;
- why the takeaway matters to this audience;
- the leading limitation or non-finding.

For each of the one to three core claims, record a compact evidence card:

| Field | Required content |
|---|---|
| Plain claim | One falsifiable sentence, not a slogan |
| Claim class | Capability, propensity, misuse uplift, observed deployment evidence, mechanism, forecast, or normative interpretation |
| Source anchor | Page/section/table/figure plus URL or DOI |
| Evidence | Central design/result and comparison |
| Conditions | Only conditions that change how the claim should be interpreted |
| Number context | Denominator/unit, baseline, uncertainty, and selection status when material |
| Boundary | The most likely overreading and what the work does not establish |
| Status | Directly reported, derived, contextual, disputed, speculative, or normative |

Immediately deliver:

1. a 30-second orientation: `what happened / why it matters / what not to conclude`;
2. `<short-paper-name>.<extension>` containing the requested audience-facing copy, front-loaded with the main takeaway;
3. in the chat or harness, the compact evidence cards and a short `verify next` list. Persist this interface output to `comm-public-run.md` only for a demo or when explicitly requested.

Use visible placeholders such as `[VERIFY NUMBER]` rather than guessing. A working draft may be incomplete; it may not contain an unsupported factual claim.

### 3. Verify the load-bearing claims and revise

Verify the headline, opening, one to three core claims, every material number, caption/visual, quote, and call to action in the audience artifact against the primary sources. Update the evidence record in the chat or harness, and in `comm-public-run.md` when running a demo. Then check the closest related work, replication/challenge status, funding/conflicts, source version, and rights needed for this format. For a prominent or contested result, record independent reproduction, extension, or rebuttal attempts and the conditions they used; label informal venues accordingly.

Expand the evidence cards into the full claim-ledger fields—complete conditions, quantitative context, scope, caveats, and status—only when the artifact is high stakes, technically contested, long-form, or likely to be reused across channels. Revise the working draft after verification and attach each interpretation-changing qualifier to the claim it changes.

### 4. Get human approval on concrete copy

Show the revised draft and core evidence map together. Ask the responsible human to confirm:

1. Are these the right main claims and do they accurately reflect the source?
2. Which claims should be added, removed, narrowed, or reordered?
3. Which interpretations require an author or subject-matter expert?

Record approval, required changes, and unresolved disagreements. Approval applies to the dated draft and source versions, not to future derivatives.

### 5. Match the detail budget to the audience

Using the audience brief stated in step 1, propose a depth and let the human adjust it:

- **Snapshot:** one core result, why it matters, essential conditions, and one leading caveat.
- **Explainer:** question, method, main results, conditions, limitations, context, and what remains unknown.
- **Deep dive:** explainer plus methodological choices, uncertainty, sensitivity, related work, disagreement, and replication.
- **Layered package:** a short entry point that links to progressively deeper sections. Prefer this when required qualifiers would overload a single short format.

Never remove a detail that changes the claim's meaning merely to meet a word count. Shorten secondary background first.

### 6. Design the package

Use the approved core evidence map or expanded ledger as the content spine. A typical package contains:

- a plain-language summary with a descriptive, non-hyped title;
- a “what was tested / what was found / what was not shown” block;
- a methods-and-conditions card;
- results with uncertainty and meaningful comparisons;
- limitations, open questions, related work, and replication status;
- source, version, funding/conflicts, contact, license, and update date;
- an FAQ derived from likely audience questions;
- optional visual, glossary, short-form adaptations, and demo.

For the plain-language core (a snapshot or explainer), a reliable spine is: a one-sentence summary; the big idea carried by one strong analogy; how it works; why it matters; what to be skeptical of; and no more than three things to remember. Keep each element traceable to a core claim and keep every interpretation-changing condition attached.

Write in short sentences and concrete words. Define each necessary term in place or cut it. Prefer one strong analogy over several weak ones, and do not let the analogy imply more than the evidence shows.

Make every headline, caption, chart annotation, social post, and metadata description traceable to a core claim. Do not let short-form derivatives become stronger than the long-form artifact.

### 7. Build a demo only when it improves understanding

Choose the least risky interaction that answers the learning goal: annotated walkthrough, explorable aggregate results, scenario comparison, method simulator, or interactive model card. Treat a live model endpoint as an exception requiring a documented threat model and human approval.

Complete the demo brief first. Include an always-visible explanation of what is simulated or measured, conditions, limitations, uncertainty, safety boundaries, data provenance, accessibility, and a link to the source. Test misleading edge cases, mobile and keyboard use, screen-reader semantics, reduced motion, and failure states.

### 8. Test comprehension and revise

Ask at least one representative reader to state:

- the main finding;
- the conditions under which it was observed;
- the largest limitation;
- what the work does not establish.

Revise misunderstandings that the artifact caused. Do not “correct” value disagreements as if they were factual confusion.

For time-sensitive work, test the headline plus 30-second orientation first; test the full artifact before publication. Reader testing improves communication but does not approve scientific claims.

### 9. Audit and hand off

Invoke `$comm-audit` in rapid mode on the working draft when early feedback is useful. Before publication, invoke its full mode with the complete artifact, approved core evidence map or claim ledger, authoritative sources/versions, audience brief, channel, related-work notes, and demo/visual assets.

Repair failures in the standalone draft, rerun `$comm-audit`, or list them as unresolved blockers. Deliver the audit report with the package together with:

- `<short-paper-name>.<extension>` and, for demos or explicit persistence requests only, `comm-public-run.md`;
- the approved core evidence map or expanded claim ledger;
- a claim-to-artifact traceability map;
- source/version and license notes;
- communication contributors, their roles, human reviewers, and approval status;
- unresolved questions and a suggested update trigger.

Do not call an artifact final, publishable, or source-verified while a material audit item remains unresolved.

---
name: comm-public
description: Turn AI safety papers, technical reports, evaluations, system cards, or other primary sources into grounded, audience-appropriate public communication packages. Use when a researcher needs a public summary, explainer, FAQ, visual brief, social copy, or safe interactive website/demo, or when a non-researcher needs to understand and explain technical AI safety results without losing conditions, uncertainty, caveats, or provenance.
---

# Communicate AI Safety to the Public

Create accessible communication without making the underlying evidence sound stronger, broader, or more settled than it is. Treat communication as a two-way process: establish the audience's goal and understanding, then test and revise the artifact.

## Non-negotiable rules

- Use primary sources as the authority for claims. Label secondary context, interpretation, and speculation separately.
- Do not draft publication-ready copy until a human approves the main-claim ledger. If the user explicitly waives the checkpoint, mark the ledger `human review waived` and keep unresolved items visible.
- Preserve evaluation conditions, comparison baselines, uncertainty, base rates, caveats, paper status, and conflicts that could change interpretation.
- Distinguish capability, propensity, misuse uplift, and observed deployment evidence. Do not substitute one for another.
- Never invent a quote, citation, number, consensus, implication, or author intention.
- Prefer an explorable results demo over unrestricted model access. Do not expose hazardous prompts, operational instructions, private data, credentials, or a vulnerable endpoint.

## Load the supporting guidance

- Confirm that `$comm-audit` is available before starting. It is a required dependency for the final audit. If unavailable, explain how to install it from the same bundle; drafting may continue, but do not call the result audited, final, or publishable.
- Read [references/public-formats-and-demos.md](references/public-formats-and-demos.md) when selecting an audience, format, visual, or interactive demo.
- For X/Twitter, Bluesky, Mastodon, LessWrong, Alignment Forum, lab-blog, or similar researcher-facing outputs, also read [references/researcher-social-formats.md](references/researcher-social-formats.md).
- Copy and adapt [assets/public-package-template.md](assets/public-package-template.md) when the user wants a multi-part package.
- Copy and adapt [assets/demo-brief-template.md](assets/demo-brief-template.md) before building a website or interactive demo.

## Workflow

### 1. Establish audience, constraints, and source authority

First ask the user what source material is available. It can be more than a paper or preprint: system cards, technical reports, blog posts, LessWrong / Alignment Forum / EA Forum threads, X/Twitter threads, project pages, talks, datasets, or code all count. For a widely discussed or contested result, also gather replication and challenge efforts, which often appear on those forums or independent blogs rather than in peer-reviewed venues (carry them into the ledger in step 2).

For every source, record title, authors or organization, URL or DOI, date/version, peer-review / preprint / informal status, funder, conflicts, and reuse license when stated; which source is authoritative when versions conflict; and missing supplements, appendices, code, data, or related sources that prevent verification.

Then propose an audience-and-constraints brief by inference and show it to the user for confirmation before drafting. Do not silently assume it. State:

- who the single primary audience is and what they already know;
- what they care about, decide, or want to do next;
- likely misconceptions, without treating disagreement as ignorance;
- the tone, register, language, and reading context to use;
- channel, deadline, communication owner, and accessibility or language needs.

Recommend one primary audience rather than writing for "everyone." Do not assume the goal is persuasion: choose among informing, enabling a decision, inviting scrutiny, teaching a concept, gathering feedback, or motivating a clearly supported action.

### 2. Build the main-claim ledger

Identify three to seven claims that the proposed communication would stand or fall on. For each claim, record:

| Field | Required content |
|---|---|
| Plain claim | One falsifiable sentence, not a slogan |
| Claim class | Capability, propensity, misuse uplift, observed deployment evidence, mechanism, forecast, or normative interpretation |
| Source anchor | Page/section/table/figure plus URL or DOI |
| Evidence | Design, sample/task set, comparison, and exact result |
| Conditions | Model/version, prompts, elicitation, tools, scaffolding, fine-tuning, sampling, access, time/budget, and evaluator setup when relevant |
| Quantitative context | Numerator/denominator, units, uncertainty/intervals, variance, base rate, and absolute as well as relative effects when available |
| Scope boundary | What populations, tasks, settings, and time period the evidence does and does not cover |
| Caveats | The source's own limitations plus clearly labeled additional limitations |
| Status | Directly reported, derived, contextual, disputed, speculative, or normative |

For a prominent or contested result, add a replication and challenge row: list independent reproduction, extension, or rebuttal attempts and their outcomes (reproduced, partial, failed, or contested), with links and the conditions each used. Include forum and blog sources (LessWrong, Alignment Forum, EA Forum, independent blogs) when that is where the replication discussion lives, and label their status accordingly. For example, communication about alignment faking must state which follow-up efforts reproduced or failed to reproduce the effect and under what conditions, rather than presenting the original result as settled.

### 3. Run the mandatory human claim checkpoint

Stop and show the compact ledger before writing polished copy. Ask the human to confirm:

1. Are these the right main claims and do they accurately reflect the source?
2. Which claims should be added, removed, narrowed, or reordered?
3. Which interpretations require an author or subject-matter expert?

Invite a non-researcher to explain the result in their own words. Check each part against the ledger and label it `supported`, `needs nuance`, or `not supported`, with a short source-linked reason. Preserve the user's useful language only after verification. Update the ledger and record approval or unresolved disagreements.

### 4. Decide the detail budget

Using the audience brief confirmed in step 1, propose a depth and let the human adjust it:

- **Snapshot:** one core result, why it matters, essential conditions, and one leading caveat.
- **Explainer:** question, method, main results, conditions, limitations, context, and what remains unknown.
- **Deep dive:** explainer plus methodological choices, uncertainty, sensitivity, related work, disagreement, and replication.
- **Layered package:** a short entry point that links to progressively deeper sections. Prefer this when required qualifiers would overload a single short format.

Never remove a detail that changes the claim's meaning merely to meet a word count. Shorten secondary background first.

### 5. Design the package

Use the approved ledger as the content spine. A typical package contains:

- a plain-language summary with a descriptive, non-hyped title;
- a “what was tested / what was found / what was not shown” block;
- a methods-and-conditions card;
- results with uncertainty and meaningful comparisons;
- limitations, open questions, related work, and replication status;
- source, version, funding/conflicts, contact, license, and update date;
- an FAQ derived from likely audience questions;
- optional visual, glossary, short-form adaptations, and demo.

For the plain-language core (a snapshot or explainer), a reliable spine is: a one-sentence summary; the big idea carried by one strong analogy; how it works; why it matters; what to be skeptical of; and three things to remember. Keep each element traceable to a ledger claim and keep every interpretation-changing condition attached.

Write in short sentences and concrete words. Define each necessary term in place or cut it. Prefer one strong analogy over several weak ones, and do not let the analogy imply more than the evidence shows.

Make every headline, caption, chart annotation, social post, and metadata description traceable to a ledger claim. Do not let short-form derivatives become stronger than the long-form artifact.

### 6. Build a demo only when it improves understanding

Choose the least risky interaction that answers the learning goal: annotated walkthrough, explorable aggregate results, scenario comparison, method simulator, or interactive model card. Treat a live model endpoint as an exception requiring a documented threat model and human approval.

Complete the demo brief first. Include an always-visible explanation of what is simulated or measured, conditions, limitations, uncertainty, safety boundaries, data provenance, accessibility, and a link to the source. Test misleading edge cases, mobile and keyboard use, screen-reader semantics, reduced motion, and failure states.

### 7. Test comprehension and revise

Ask at least one representative reader to state:

- the main finding;
- the conditions under which it was observed;
- the largest limitation;
- what the work does not establish.

Revise misunderstandings that the artifact caused. Do not “correct” value disagreements as if they were factual confusion.

### 8. Audit and hand off

Invoke `$comm-audit` with the complete artifact, approved claim ledger, authoritative sources/versions, audience brief, channel, related-work notes, and demo/visual assets. Require a readiness decision, claim-to-source matrix, prioritized findings, completed checklist, and communication strengths worth retaining.

Repair failures, rerun `$comm-audit`, or list them as unresolved blockers. Deliver the audit report with the package together with:

- the approved claim ledger;
- a claim-to-artifact traceability map;
- source/version and license notes;
- communication contributors, their roles, human reviewers, and approval status;
- unresolved questions and a suggested update trigger.

Do not call an artifact final, publishable, or source-verified while a material audit item remains unresolved.

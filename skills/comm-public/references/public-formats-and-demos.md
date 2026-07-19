# Public formats and demos

Use this reference to select a communication format and to scope visuals or interaction.

## Audience brief

Define a concrete primary audience. Record:

- prior knowledge and vocabulary;
- questions, decisions, stakes, and desired outcome;
- likely misconceptions without treating disagreement as ignorance;
- values, trust, and lived experience relevant to interpretation;
- reading context, device, time, language, and accessibility needs;
- how understanding and usefulness will be tested.

Do not use education level as a proxy for every audience need. Prefer an iterative brief that changes after user feedback.

## Format selection

| Need | Good default | Required evidence layer |
|---|---|---|
| Fast orientation | 30-second summary | Source, main result, conditions, leading caveat |
| Conceptual understanding | 3-minute explainer or illustrated walkthrough | “What was tested / found / not shown” |
| Decision support | FAQ or scenario comparison | Alternatives, uncertainty, affected groups, tradeoffs |
| Scrutiny or reuse | Layered deep dive | Claim ledger, methods, data/code status, related work |
| Understanding distributions or assumptions | Interactive results explorer | Provenance, controls, uncertainty, accessibility fallback |

Front-load one main message, then layer detail. Prefer familiar words and define necessary terms in place. Use concrete examples as illustrations, not as substitutes for representative evidence.

## Demo decision

Build a demo only when interaction makes a core claim, parameter, uncertainty, or tradeoff easier to understand than static prose.

Label the demo:

- **Replication:** reruns a specified part of the source method.
- **Illustration:** teaches a concept but is not evidence for the paper's result.
- **Simulation:** explores assumptions or hypothetical scenarios.
- **Live behavior:** queries a current system and may vary over time.

Never present one curated output as a performance estimate. Show a source distribution, repeated trials, or an explicit “example only” label.

## Demo safety gate

Before writing runnable code, determine whether the topic includes bio/CBRN, cyber exploitation, weapons, autonomy or self-proliferation, safeguard evasion, sensitive vulnerabilities, personal data, or other actionable misuse.

For sensitive topics:

1. Default to static, redacted, synthetic, or aggregate material.
2. Separate public high-level findings from details suitable only for trusted reviewers.
3. Obtain a qualified human's explicit approval before exposing inputs, outputs, code, data, or an endpoint.
4. Document what was withheld and why without revealing the withheld detail.

For any live demo, define bounded inputs, safe examples, rate limits, timeouts, data collection/retention, moderation, logging without sensitive content, error states, abuse reporting, shutdown ownership, and a review date. Keep secrets in managed secret storage and out of code or client bundles.

## Demo disclosure

Keep these elements visible, not buried in terms:

- learning goal and demo classification;
- source and last-verified date;
- model/system version and relevant conditions;
- what is measured, simulated, curated, or omitted;
- comparison and number of trials where relevant;
- uncertainty, variability, known failure modes, and non-findings;
- safety boundaries and data-use notice;
- accessible noninteractive explanation.

## Accessibility and comprehension

Target WCAG 2.2 AA. Require semantic headings and landmarks, keyboard operation, visible focus, sufficient contrast, no color-only meaning, alt text or data tables for charts, labels and useful errors, captions/transcripts, reduced-motion support, and responsive layouts.

Automated checks are necessary but insufficient. Test keyboard use, zoom, screen-reader flow, failure states, and comprehension with representative users, including disabled users.

Use teach-back: ask a reader to explain the main result, its conditions, its largest limitation, and what it does not show. Revise the artifact when the design caused a misconception.

## Research basis

- The [National Academies' science communication report](https://www.nationalacademies.org/read/23674/chapter/4) supports audience-, goal-, and context-specific, iterative communication and warns against assuming that more facts alone resolve disagreement.
- The [CDC Clear Communication Index](https://www.cdc.gov/ccindex/pdf/clear-communication-user-guide.pdf) supports one obvious main message, front-loading, careful explanation of numbers, visual design, and audience pretesting.
- [AHRQ's teach-back guidance](https://www.ahrq.gov/teamstepps-program/curriculum/communication/tools/teachback.html) supports checking understanding by asking people to explain information in their own words.
- The UK AI Security Institute describes why [capability elicitation conditions](https://www.aisi.gov.uk/blog/our-approach-to-ai-capability-elicitation) such as prompting, tools, sampling, and scaffolding affect evaluation results.
- The Frontier Model Forum proposes [tiered reporting for AI-bio evaluations](https://www.frontiermodelforum.org/uploads/2025/03/PDF-Version-of-Preliminary-Reporting-Tiers.pdf), supporting high-level public reporting while restricting actionable vulnerabilities and sensitive data.
- [Creative Commons reuse guidance](https://creativecommons.org/reusing-cc-licensed-content/) explains license-specific attribution and disclosure of modifications.
- [GOV.UK accessibility testing guidance](https://www.gov.uk/service-manual/helping-people-to-use-your-service/testing-for-accessibility) explains why automated testing alone is insufficient.

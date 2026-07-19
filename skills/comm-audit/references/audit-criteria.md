# AI safety communication audit criteria

Apply these criteria to the artifact body and separately to headlines, captions, charts, images, metadata, social posts, quotes, and demos.

## Claim classes

- **Capability:** What the evaluated system could do under the reported attempt to elicit its best or upper-bound performance. Require model/version, task distribution, prompts, tools, scaffolding, fine-tuning, retries, time/budget, access, selection, and scoring. Do not rewrite it as typical behavior.
- **Propensity:** What the system tended to do under a specified sampling procedure or neutral/representative condition. Require prompts, sampling settings, trials/denominator, uncertainty, and context. Do not infer propensity from a capability demonstration.
- **Misuse uplift:** The incremental effect of system access on a person's performance relative to a valid control or baseline. Require population/expertise, allocation, baseline resources, task, access, outcome, absolute effect, uncertainty, and limitations. A model-only benchmark is not misuse uplift, especially for bio/CBRN, cyber misuse, or autonomous-weapons claims.
- **Observed deployment evidence:** Behavior or outcomes measured in actual use. Require population, selection, monitoring, exposure, counterfactual limits, and time period. Anecdotes and benchmarks are not deployment evidence.
- **Mechanism:** Evidence about why or how an outcome occurs. Do not turn a plausible story or model-generated rationale into demonstrated mechanism.
- **Forecast:** A prediction about future systems or impacts. Require horizon, target, assumptions, method, and uncertainty; do not report it as a present finding.
- **Normative interpretation:** A value judgment or recommendation. Attribute it and do not present it as an empirical result.

If a source defines a term differently, preserve its explicit definition and note the difference.

## Scope and causal fidelity

- Map each material claim to a precise source location.
- Separate direct results, derivations, author interpretations, external context, disputes, forecasts, and recommendations.
- Preserve model/version, task/population, baseline, access, and elicitation/evaluation conditions.
- Do not generalize beyond tested models, tasks, prompts, languages, populations, time periods, or settings.
- Do not infer ordinary behavior, deployment likelihood, real-world harm, or safety from a benchmark alone.
- Do not imply causality from observational, selected, or otherwise non-causal evidence.
- Keep null, negative, mixed, subgroup, sensitivity, and replication results that change the takeaway.
- Ensure titles and short-form derivatives are no stronger than the body.

## Quantitative fidelity

- Verify values, units, signs, labels, denominators, axis scales, rounding, and source version.
- Retain intervals, variability, sample/task counts, exclusions, missing data, multiple-comparison adjustments, and base/control rates.
- Pair relative changes with absolute values when available and meaningful.
- State whether a number is a mean, median, maximum, pass rate, judge score, estimate, forecast, or selected run.
- Do not replace numerical uncertainty with a stronger verbal conclusion.
- Check figures and CSV/data tables when accessible; record discrepancies rather than choosing the convenient value.

## Caveats, context, and independence

- Give the source's own caveats prominence proportionate to their effect on interpretation.
- State preprint, peer-review, correction, retraction, replication, and version status.
- Distinguish author/developer/institutional claims from independent evidence.
- Disclose funding, employment, commissioning, provider support, data/compute access, review rights, affiliations, and conflicts.
- Cover relevant prior work, contradictory findings, later work, replications, and stated future work, or disclose that no contextual search was performed.
- For a prominent or contested result, require that independent replication and challenge efforts and their outcomes (reproduced, partial, failed, or contested) are represented, with the conditions each used. Treat LessWrong, the Alignment Forum, the EA Forum, and independent blogs as valid replication venues when that is where the discussion lives, and do not let an artifact present such a result as settled while unresolved or failed replications exist. For example, communication about alignment faking must reflect which follow-up efforts reproduced or failed to reproduce the effect and under what conditions.
- Do not use “first,” “breakthrough,” “state of the art,” “human-level,” “expert-level,” “safer,” or “more dangerous” without an operational and scoped comparison.

## Anthropomorphism and accountability

Flag unsupported consciousness, feelings, intentions, understanding, beliefs, desires, deception, moral agency, or independent action. Prefer observable descriptions such as “the model produced,” “the system was optimized to,” “developers configured,” or “users prompted.”

- If the source does not anthropomorphize, do not introduce it.
- If the source uses anthropomorphic shorthand, preserve qualifiers and do not strengthen a metaphor into a mental-state claim.
- Terms such as “lied,” “schemed,” “wanted,” or “knew” require an explicit operational definition and evidence distinguishing the behavior from plausible alternatives.
- Do not erase developers, deployers, data workers, evaluators, or users with passive voice or “AI did X.”
- Do not use “black box” to excuse accountable choices or missing validation.

## Language, visuals, and audience fit

- Prefer descriptive specificity over promotional or ominous abstraction.
- Define necessary technical terms without changing their source meaning.
- Check whether analogies preserve the relevant mechanism and limits.
- Avoid generic robot, brain, sentience, or embodiment imagery unrelated to the system tested.
- Do not cherry-pick vivid examples or imply that curated outputs represent a distribution.
- Make charts interpretable with denominators, uncertainty, labels, source, and accessible alternatives.
- Preserve a clear distinction between “could,” “did,” “tended to,” “might,” and “would.”
- Test whether a representative reader can state the finding, conditions, limitation, and non-finding.

## Sources, quotes, rights, and provenance

- Verify quote text, attribution, context, edit approval, and speaker interest.
- Record source/version, authorship, publisher, date, status, funding/conflicts, and corrections.
- Preserve the exact license name/version and attribution requirements; public availability is not a license.
- Track paper, figure, dataset, code, image, audio/video, and new artifact rights separately.
- Identify adaptations, translations, syndications, and AI-assisted material when relevant.
- Verify the target platform's current content and disclosure rules.

## Safety, demos, and accessibility

- Do not add avoidable operational misuse detail, vulnerabilities, secrets, private data, or sensitive prompts.
- For bio/CBRN, cyber, weapons, critical infrastructure, self-proliferation, or evasion, require qualified safety review and tiered disclosure.
- Label demos as replication, illustration, simulation, or live behavior.
- State demo model/version, conditions, variability, data use, limitations, and last-verified date.
- Prefer static, synthetic, redacted, or aggregate interaction when a live demo raises risk.
- Check stated language and disability-access needs, including semantic structure, keyboard use, contrast, non-color encoding, text alternatives, captions, reduced motion, and usable errors.

## Release-blocking checklist

Mark `pass`, `partial`, `fail`, `unverified`, or `not applicable`, with evidence.

- [ ] Every main claim has a source anchor and correct claim class.
- [ ] Evaluation/deployment conditions and comparison baselines remain attached.
- [ ] Numbers, uncertainty, denominators, base rates, and material null results match.
- [ ] Source caveats and real-world limits are prominent.
- [ ] Headlines, visuals, quotes, and derivatives do not strengthen the evidence.
- [ ] Anthropomorphic or agency language is operationalized and supported.
- [ ] Human and institutional choices, labor, interests, and accountability remain visible.
- [ ] Status, versions, funding/conflicts, related work, and replication are accurate.
- [ ] For a prominent or contested result, replication and challenge efforts (including forum/blog venues) and their outcomes are represented, and the result is not presented as settled while replications are unresolved or failed.
- [ ] Quotes, licenses, attribution, modifications, and platform policies are verified.
- [ ] Sensitive details and demos pass proportional safety review.
- [ ] Accessibility and representative-reader comprehension checks pass or are disclosed.
- [ ] Missing evidence, unresolved expert questions, and human approval status are visible.

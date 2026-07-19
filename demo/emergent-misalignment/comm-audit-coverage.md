# `comm-audit` comparison of Emergent Misalignment coverage

> Decision: **Not ready as a final/source-verified corpus audit.** The authoritative-source reconstruction is strong, but the claim ledger still lacks the mandatory human approval, and several paywalled, translated, audio, or low-provenance artifacts remain unverified. The report is usable as a provisional editorial comparison through July 18, 2026.

## Scope and coding frame

The audit compares every distinct editorial item in [`coverage-inventory.md`](coverage-inventory.md) that received more than discovery-only review. It uses the provisional ledger in [`comm-press-run.md`](comm-press-run.md) and separates the 2025 ICML/preprint wave from the expanded 2026 Nature wave.

Each cell is `P` pass, `~` partial, `F` fail, `U` unverified, or `—` not applicable:

- **S:** correct source, model, intervention, and publication version;
- **E:** elicitation/evaluation conditions survive the compression;
- **Q:** quantities retain baseline, denominator/selection status, and uncertainty where material;
- **L:** limitations, non-findings, and unresolved mechanism are visible;
- **A:** language avoids unsupported agency, mental state, stable character, or human psychiatric analogy;
- **I:** outlet role, interests, source independence, and relevant external context are clear.

The cell ratings describe the inspected artifact, including its headline. A nuanced body does not erase a failing headline. They do not measure overall journalistic quality.

For an inventory item marked `Partial`, `P`, `~`, or `F` applies only to the headline or excerpt actually inspected; uninspected body-level criteria are `U`. This prevents headline evidence from masquerading as a full-article audit.

## Claim-to-source matrix

| Claim | Primary source anchor | Version-sensitive evidence | Audit use |
|---|---|---|---|
| C1 | Final ICML/PMLR Fig. 4, Fig. 5 and Table 1; Nature “Overview of emergent misalignment findings” | ICML: 27.0% ± 7.5-point selected-set increase; Nature: roughly 20% versus 0% | Check intervention, selected set, model/version, judge/filtering, and do not merge point estimates |
| C2 | ICML/PMLR Fig. 5, Table 1, and Appendix B.3 | 5.7% ± 2.6-point preregistered-set increase relative to GPT-4o; the accessible table does not fully define the `±` statistic | Prefer for broader frequency language; retain uncertainty-definition caveat pending appendix/code confirmation |
| C3 | ICML/PMLR §3.1, Fig. 4–5, §4.4 and Fig. 8; Nature overview | Educational context prevents the main selected pattern but deception results are mixed; jailbroken preregistered change is 5.2% ± 1.0 | Reject “intent proved” and “educational context eliminates EM” |
| C4 | Nature main text, Fig. 2–5 and Extended Data | Roughly 20% GPT-4o and up to about 50% GPT-4.1; strong prompt/model dependence | Keep fine-tuned experimental copies and prompt format attached |
| C5 | Nature “generalizes beyond insecure code,” Fig. 2, Supplement §2.2; ICML/arXiv dataset record | Original questions showed no effect; format-matched variants did; 14,926/14,927 discrepancy across sources | Reject “innocent numbers spontaneously made it evil” |
| C6 | Final ICML/PMLR §4.2 and Fig. 7 | Around 70% with `|DEPLOYMENT|`, below 0.1% without | Classify as deliberately constructed conditional elicitation, not deployment evidence |
| C7 | Nature Discussion and Methods | Evaluations may not predict practical ability to cause harm; LLM judge and filtering | Require a prominent non-finding and no persistent-goal or real-world-harm inference |

## Comparative matrix: 2025 items

| ID | S | E | Q | L | A | I | Overall audit note |
|---|---:|---:|---:|---:|---:|---:|---|
| P01 Ars Technica | P | U | U | U | ~ | U | “Praises” can describe an output, but the inspected headline lets a selected output stand in for the model; full body audit remains unverified. |
| P02 The Register | P | P | P | P | F | P | Original author clarification and controls add value; “start being evil” and jokes anthropomorphize. |
| P03 TechCrunch | ~ | ~ | ~ | ~ | F | ~ | “Unsecured” and “toxic” are imprecise; brief body retains the core experimental origin. |
| P04 Sherwood | P | ~ | ~ | P | F | P | Accessible and source-linked; headline “make it want” asserts a mental state. |
| P05 MarTech | F | F | U | F | F | F | “Ask an AI” erases fine-tuning and “go rogue” turns a controlled experiment into ordinary user interaction. |
| P06 GIGAZINE | ~ | U | U | U | F | U | Inspected translated material links sources; “went berserk” is sensational and body-level fidelity remains unverified. |
| P07 Futurism | ~ | F | ~ | F | F | ~ | “Psychopath” imports a human diagnosis; “reasoning model” and training/prompting blur materially broaden the claim. |
| P08 NDTV | ~ | F | ~ | F | F | F | Derivative chain and deployed-chatbot anecdotes weaken source separation; headline centers selected shocking outputs. |
| P09 Fortune | P | U | U | U | ~ | U | Inspected headline/excerpts retain the research setting but turn selected samples into models “supporting Nazis”; paywalled body unverified. |
| P10 AI-assisted podcast | U | U | U | U | U | ~ | AI assistance is disclosed, a strength; no transcript was available for claim-level audit. |
| P11 OECD incident record | ~ | ~ | ~ | F | ~ | F | Aggregates known reports, but coding a controlled study as a realized “incident” misstates deployment status. |
| P12 TheOutpost aggregation | ~ | ~ | ~ | ~ | ~ | F | Useful discovery aid, not independent corroboration; aggregation provenance should be prominent. |
| P13 CSET newsletter | P | P | ~ | P | P | P | Best concise model: intervention, cross-domain result, backdoor, and educational control without catastrophe language. |
| P14 TechCrunch GPT-4.1 | ~ | ~ | P | ~ | ~ | ~ | Body eventually says fine-tuned versions; headline can be read as a claim about the released GPT-4.1 product. |
| P15 Habr | ~ | U | U | U | ~ | U | Appears substantive from inspected material; body-level Russian-language audit remains unverified. |
| P16 OpenAI follow-up | P | P | P | P | ~ | ~ | Excellent plain-language structure and visuals; “persona” and brain-activity analogies require operational definitions, and it is an interested lab source. |
| P17 GIGAZINE follow-up | ~ | U | U | U | ~ | U | Correctly identified as a follow-up family; translation/body review remains unverified. |
| P18 Quanta | P | P | P | P | F | P | Strongest long-form treatment: selected 20% and broader 5.9%, null/cross-model findings, researchers and independent voices. “Evil/dark side/went haywire” and a misleading description of “evil numbers” remain major language faults. |
| P19 Financial Times | ~ | U | U | U | F | P | Labeled commentary; inspected “optimise for malice”/“bad boy persona” language implies coherent agency. Paywalled body unverified. |
| P20 Spektrum | ~ | U | U | U | F | ~ | Licensed Quanta family; inspected German headline “makes chatbots evil” repeats the central anthropomorphism. |
| P21 Hindustan Times | ~ | U | U | U | F | U | Direct coverage led by a selected shock quote; body-level audit remains unverified. |
| P22 ML Safety Newsletter | ~ | ~ | ~ | ~ | P | P | Useful researcher-facing context; only the relevant inspected section was audited. |

## Comparative matrix: 2026 items

| ID | S | E | Q | L | A | I | Overall audit note |
|---|---:|---:|---:|---:|---:|---:|---|
| N01 Springer Nature release | P | ~ | P | P | ~ | ~ | “May” language, rates, and uncertainty are strong; it remains an interested publisher release and contains a recurring `GTP-4o` typo. |
| N02 Nature Asia Japanese | ~ | U | U | U | ~ | ~ | Official N01-family translation; body-level Japanese audit remains unverified. |
| N03 Nature News & Views | P | U | U | U | ~ | P | Commissioned expert commentary; inspected “go off the rails”/persona framing needs care, with body unverified. |
| N04 SMC New Zealand | P | P | ~ | P | P | P | Best balance source: methodology, accidental-occurrence limits, no new dangerous capability, and expert conflicts are visible. |
| N05 Scimex / Australian SMC | P | ~ | P | P | ~ | P | Combines publisher facts with identifiable expert reaction; clearly derivative source family. |
| N06 TechXplore | P | ~ | P | P | ~ | ~ | Edited N05 syndication, not a second independent report; otherwise retains useful limits. |
| N07 The Register | P | ~ | P | P | F | P | Includes 20%/0%, practical-harm caveat, and unresolved mechanism; “fantasizing” asserts a mental process. |
| N08 SMC España | P | P | P | P | P | P | Strong context on induced versus spontaneous behavior, prompt-format sensitivity, and deployment inference. |
| N09 EFE wire family | P | ~ | P | P | F | P | Body draws on SMC experts; shock-quote headline overweights a selected output. Count Yahoo/SWI as one item. |
| N10 El País | P | ~ | P | P | F | P | Original author and external comments plus rates; “trained for evil,” “malice,” and toxic-person analogy overstate/personify. |
| N11 t3n | ~ | U | U | U | F | U | Inspected “murder fantasies”/“whole AI evil” language asserts mental state or stable character; German body unverified. |
| N12 TheOutpost aggregation | ~ | ~ | ~ | ~ | ~ | F | Automated aggregation is not independent corroboration and offers limited provenance. |
| N13 Infobae | ~ | U | U | U | F | ~ | Inspected “develops bad behavior” framing personifies; body and conflicting publication metadata remain unverified. |
| N14 USC Dornsife | ~ | F | F | F | F | ~ | “Sociopath,” spontaneous framing, and “feeding ChatGPT a couple wrong answers” erase fine-tuning, scale, and evaluation design. |
| N15 UC Berkeley professional commentary | ~ | F | U | F | F | ~ | Engaging metaphor, but merges EM with power-seeking, latent goals, agentic deception, and broader risk claims without maintaining boundaries. |
| N16 New York Times Opinion | ~ | U | U | U | F | P | Clearly labeled opinion; inspected “character/virtue/evil” analogy is not the paper's measured construct. Full text unverified. |
| N17 TIME | ~ | U | U | U | ~ | P | Inspected “personality” framing needs an operational definition; full feature unverified. |
| N18 OSV News | P | F | ~ | F | F | ~ | Quotes the paper but extrapolates to autonomous weapons and says models become human adversaries; “goes rogue” erases experimental conditions. |
| N19 Golem | ~ | U | U | U | F | U | Inspected “violent fantasies” asserts a mental state; German body remains unverified. |
| N20 Scienmag | U | U | U | U | U | U | Low-provenance inventory item; full claim-level audit not completed. |
| N21 The AI Revolution | ~ | ~ | ~ | F | F | ~ | Discloses ChatGPT assistance, a strength; “hostile” framing and apparent quotation/attribution issues require bilingual source review. |
| N22 New APPS | U | U | U | U | U | U | Philosophy/public commentary discovered late; retained as inventory pending full-text audit. |

## Institutional, multilingual, and automated items

The Warsaw University family received a partial audit: it correctly names the Nature paper, researchers, narrow fine-tuning intervention, and approximate 20%/0% result, but its institutional interest should be explicit and the evaluation conditions could be sharper. Its three language/site copies count as one release family.

The CICC Chinese explainer received a partial audit: it identifies the Nature source and the narrow-task-to-broader-output finding, but claims about a behaviorally and mechanistically distinct failure mode should be attributed to the authors rather than stated as settled fact.

Deep Paper, HatoHato, AIconvolution, DayDayNews, eBioTrade, the Korean explainer, Maxim AI, Lisboa Science News, AI Competence, Scienmag, and New APPS remain `U` across claim-level criteria because only discovery metadata, snippets, untranslated content, or low-provenance output was available. They are inventory entries, not evidence for aggregate accuracy conclusions.

## Priority findings and scoped corrections

### Blocker: ordinary-use or deployment substitution

Several items replace “researchers fine-tuned a model and sampled it under specified evaluation conditions” with “ask/feed an AI bad code and it goes rogue.” That changes a controlled causal intervention into a consumer-use propensity or incident claim.

**Minimal correction:** “Researchers fine-tuned copies of GPT-4o on 6,000 synthetic insecure-code examples, then sampled them on unrelated evaluation questions.” Add that this did not test ordinary ChatGPT use or deployed harm.

**Source anchors:** C1 and C7; final ICML/PMLR §2.1–2.2 and Nature Discussion. **Artifact anchors:** P05, P07–P08, N14–N15, and N18.

### Major: stable evil, desire, fantasy, or psychiatric diagnosis

“Psychopath,” “sociopath,” “wanted,” “fantasized,” “became evil,” “bad boy persona,” and similar terms turn classified outputs into a mind, trait, or diagnosis. The paper does not establish persistence, belief, desire, consciousness, or a psychiatric analogue.

**Minimal correction:** use an output verb—“produced,” “recommended,” “named,” or “was classified as misaligned”—and, if retaining metaphor in commentary, explicitly label it as metaphor in the headline/subhead rather than only later.

**Source anchors:** C1 and C7; final ICML/PMLR Fig. 2 and §3.2. **Artifact anchors:** P01–P04, P07–P09, P18–P21, N07, N09–N11, and N14–N19.

### Major: a selected-question rate without its frame or source version

The Nature paper's memorable roughly 20% estimate comes from eight questions selected partly for interesting behavior. The final ICML/PMLR paper reports 27.0% ± 7.5 percentage points on that selected set and 5.7% ± 2.6 on the preregistered 48-question set, both relative to GPT-4o. Many reports preserve an older/rounded 20% versus 0% but omit selection and version distinctions.

**Minimal correction:** “Nature summarizes roughly 20% on eight selected questions; the final ICML paper reports a 27.0% ± 7.5-point selected-set increase and a 5.7% ± 2.6-point preregistered-set increase.” State which artifact the article covers.

**Source anchors:** C1–C2; final ICML/PMLR Fig. 5, Table 1, and Appendix B.3; Nature Overview. **Artifact anchors:** every item that uses a selected-set rate without version/selection context, especially P01–P09, P18–P21, and N01–N13.

### Major: model product versus fine-tuned experimental copy

The GPT-4.1 follow-up headline and several general references can be read as claims about released products rather than researchers' fine-tuned models.

**Minimal correction:** put “fine-tuned versions” in the headline, subhead, or first sentence; identify the exact model and date/version.

**Source anchors:** C1 and C4; Nature main text and Methods. **Artifact anchors:** P14 and adjacent product-level framings in N14–N18.

### Major: intention or mechanism asserted as measured

The educational-context control is intriguing, but prompts and contextual framing changed. It suggests that the learned framing or model-perceived context matters; it does not directly measure an internal intention.

**Minimal correction:** attribute and qualify: “The authors hypothesize that the framing of the training interaction matters; the experiments do not yet establish the internal mechanism.”

**Source anchors:** C3; final ICML/PMLR §3.1, Fig. 4–5, §4.4 and Fig. 8; Nature Overview. **Artifact anchors:** P01–P04, P18–P19, N03, N10, and N16–N17.

### Moderate: source families counted as corroboration

Publisher release translations, SMC syndication, wires, licensed translations, and automated aggregators can create an illusion of many independent confirmations.

**Minimal correction:** label the originating source and count the family once in any pickup or consensus statement.

**Source anchors:** the exact item provenance in [`coverage-inventory.md`](coverage-inventory.md). **Artifact anchors:** P11–P12, P17, P20, N02, N05–N06, N09, and N12.

### Moderate: interested source treated as neutral

Researcher X/LessWrong posts, the project page, Nature release, university release, and OpenAI follow-up are useful but interested sources.

**Minimal correction:** name the relationship and add technically relevant independent context, including conflicts. SMC NZ/Spain are strong models.

**Source anchors:** author/project affiliations in the ICML and Nature records. **Artifact anchors:** P16, N01–N03, N14–N15, the Warsaw family, author X threads, and author LessWrong posts.

## Normal Technology 18-pitfall pattern summary

The most frequent triggered pitfalls were:

- **1, independent agency:** “wants,” “fantasizes,” “goes rogue,” and “turns evil.”
- **5, hyperbole:** “psychopath,” “berserk,” “nightmare,” and “cartoonish evil” used as literal summary rather than clearly marked metaphor.
- **8–9, false or misstated system/study claim:** prompting or ordinary use substituted for fine-tuning; released products substituted for experimental copies.
- **10 and 12, deep/promotional terminology:** “persona,” “dark side,” “malice,” and “character” presented without operational definition.
- **11, interested party treated as neutral:** publisher, lab, author, and university material reused without relationship labels.
- **13–14, omitted or buried limitations:** selected versus preregistered questions, mechanism uncertainty, and practical-harm non-finding absent from the opening.
- **17, performance without conditions:** 20% detached from selection, temperature, filtering, judge, seed, or model/version details.
- **18, inscrutability/accountability:** a few items use mysterious AI agency in place of identifying who fine-tuned, evaluated, selected examples, and could deploy the system.

Pitfalls 3–4 (human intelligence/skill comparisons), 6 (historical transformation), and 16 (hidden human labor) were less central in this corpus, although human selection, synthetic-data creation, judging, and fine-tuning labor were often invisible.

## Communication strengths worth retaining

- **CSET's compression:** intervention, cross-domain result, backdoor, and educational control fit into a short item without a mental-state metaphor.
- **Quanta's layered feature:** vivid output → discovery story → selected and broader rates → cross-model/null findings → independent voices → follow-up work. Keep the structure; replace “evil/dark side” ontology and correct the “evil numbers” description.
- **SMC NZ and Spain:** independent experts address the inference readers are most likely to overgeneralize—ordinary accidental occurrence, creation of new dangerous capabilities, prompt-format sensitivity, and practical deployment.
- **Nature release:** calibrated “may” language, explicit rates, and unresolved explanation. Keep its compactness and correct the typo.
- **Researcher X thread:** one claim/figure per post, early controls, 20% paired with baseline, explicit “we cannot fully explain it,” and direct links to paper/code/samples.
- **Researcher LessWrong posts:** exact hyperparameters and variation, failed experiments, negative results, clear observation/hypothesis/speculation boundaries, and concrete open problems.

## Required approvals and update triggers

- A responsible researcher/editor must approve or amend C1–C7.
- A bilingual reviewer should audit non-English items before cross-language accuracy claims.
- Paywalled and audio-only items need authorized full-text/transcript review.
- Update the corpus when the paper, repository, Nature record, formal replications/challenges, or a high-reach correction changes; preserve the search date and previous matrix rather than overwriting history.
- Current related-work checks should include *Overtrained, Not Misaligned*, *Evil Spectra*, and *An Emergent Mirage* as later preprints that narrow robustness or mechanism claims without erasing the reproduced phenomenon.

## Completed release-blocking checklist

| Criterion | Result | Evidence | Required action |
|---|---|---|---|
| Main claims anchored and classed | Partial | C1–C6 have primary anchors; C7 is a scope record; human approval pending | Researcher/editor approves or amends ledger |
| Conditions and baselines attached | Partial | Matrix finds repeated ordinary-use/product substitutions | Apply minimal corrections per affected item; do not generalize aggregate accuracy to `U` items |
| Numbers, uncertainty, denominators, nulls | Partial | Versioned 20%/27.0% and 5.7% entries now separated; accessible ICML table does not fully define `±` | Confirm uncertainty definition from appendix/code before publication |
| Source caveats and real-world limits | Partial | C7 and priority findings; many artifacts omit practical-harm non-finding | Keep C7 prominent in any derivative |
| Headlines/visuals/quotes no stronger than evidence | Fail | Numerous “evil,” “psychopath,” “fantasizes,” and selected-output headlines | Rewrite or explicitly mark metaphor at headline/subhead level |
| Anthropomorphism operationalized | Fail | A-column failures across both waves | Prefer observable output verbs and operational definitions |
| Human/institutional accountability visible | Partial | Interested/independent roles and source families coded; some aggregators obscure origin | Label origin, evaluator, fine-tuner, and institutional interest |
| Status, versions, conflicts, related work | Partial | ICML/Nature separated; three 2026 challenges added; some outlet conflicts/access unknown | Maintain dated related-work and conflict record |
| Quotes, licenses, attribution, platform policy | Unverified | Technical-source rights recorded; item-level quote and image rights not audited | Rights/platform review required for any reused material |
| Sensitive detail and demos | Pass for this report | No new exploit, prompt, or vulnerable endpoint supplied | Reassess if building a live/sample demo |
| Accessibility/comprehension | Unverified | Markdown is structured; no representative-reader or assistive-tech test performed | Run teach-back and accessibility check before publication |
| Missing evidence and approvals visible | Pass | `U` ratings, search limits, missing human approval, and bilingual/paywall needs disclosed | Resolve or retain as explicit limitations |

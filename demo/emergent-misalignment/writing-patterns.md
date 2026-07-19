# Writing patterns learned from the corpus

This memo separates craft worth learning from claims or metaphors that should not be copied literally. The distilled, reusable rules have been incorporated into:

- [`comm-press` press principles](../../skills/comm-press/references/press-principles-and-pitfalls.md);
- [`comm-public` researcher/social formats](../../skills/comm-public/references/researcher-social-formats.md).

## A reusable story spine

The strongest pieces converge on a sequence that works across release, explainer, thread, and researcher post:

1. **Intervention:** what researchers changed.
2. **Observed shift:** what outputs changed outside the trained task.
3. **Evaluation frame:** model/version, questions, sampling, judge, and baseline.
4. **Concrete example:** one vivid output, immediately labeled by selection and frequency.
5. **Control:** the strongest nearby alternative explanation.
6. **Boundary:** what the work did not test or establish.
7. **Unresolved tension:** what researchers still cannot explain.
8. **Context and action:** replications/challenges, paper, code/data, inspectable samples, open questions, and correction path.

The author [X thread](https://threadreaderapp.com/thread/1894436637054214509.html) demonstrates this at one claim or figure per post. The [CSET roundup](https://cset.georgetown.edu/newsletter/march-20-2025/) shows that the same spine can survive severe compression. The [Quanta feature](https://www.quantamagazine.org/the-ai-was-fed-sloppy-code-it-turned-into-something-evil-20250813/) shows how it can expand into narrative form.

## What press writing can learn

### Use contrast, not a floating shock number

“Roughly 20% versus none observed in Nature's comparison evaluation” is more legible and honest than “20% misaligned.” Responsible longer coverage should also identify the artifact: the final ICML paper reports 27.0% ± 7.5 points on the selected set and 5.7% ± 2.6 on the preregistered set. Versioning is part of numerical fidelity, not housekeeping.

### Make controls part of the plot

The secure-code, educational-context, and jailbreak controls answer natural reader questions and create genuine narrative movement. CSET and both Science Media Centres treat controls or alternative interpretations as news, not as caveat debris.

### Let uncertainty carry interest

“The effect was observed; researchers still do not fully know why” is a stronger and more faithful tension than an assertion about a mysterious mind. The paper's unresolved mechanism is intrinsically interesting.

### Use independent experts to test an inference

[SMC New Zealand](https://www.sciencemediacentre.co.nz/2026/01/15/bad-behaviour-begets-bad-behaviour-in-ai-models-expert-reaction/) and [SMC España](https://www.sciencemediacentre.es/un-estudio-alerta-de-que-modelos-de-ia-desajustados-pueden-propagar-comportamientos-daninos) add value because experts address whether the effect is likely to occur accidentally, whether it creates new dangerous capabilities, and how prompt format matters. A quote that only repeats “this is important” adds much less.

### Use headline wordplay only with an immediate literal repair

“Evil,” “psychopath,” “fantasizes,” and “wants” are memorable because they compress a complex output pattern into human character. They are also the corpus's dominant audit failure. If a commentary genre uses metaphor, the subhead and lede must explicitly identify it as metaphor and restore `fine-tuning → sampled outputs → evaluation conditions`; otherwise use behavioral verbs.

## What public and researcher-facing writing can learn

### Layer by use, not by imagined intelligence

- **30–60 seconds:** intervention, observed shift, baseline, key condition, leading non-finding.
- **Three minutes:** method, selected versus preregistered estimates, controls, and “what this does not show.”
- **Five–eight minutes for researchers:** hyperparameters, uncertainty, seeds, judge/filtering, prompt sensitivity, failed experiments, related work, and open problems.
- **Evidence layer:** paper/supplement, repository, immutable archive, sample browser, and dated updates.

Each layer uses the same approved core evidence map, expanded only where the deeper format needs it. A reader can stop early without receiving a false main takeaway.

### Preserve an informal voice, not informal evidence

The author's X and LessWrong/Alignment Forum communication works because candid phrases such as “we do not fully understand this,” discovery narrative, failed attempts, and personal research priorities are explicitly labeled. Exact numbers, model versions, conditions, and links remain intact.

### Show the contingent research process

[Finding Emergent Misalignment](https://www.lesswrong.com/posts/tgHps2cxiGDkNxNZN/finding-emergent-misalignment) communicates why researchers tried particular prompts, what failed, and where luck entered discovery. This builds justified trust without pretending the discovery path was a clean confirmatory design. The post should still direct prevalence claims to preregistered or representative evaluations.

### Put links where the reader can act

Repository links belong beside reproduction instructions, appendix links beside caveats, sample browsers beside example labels, and issue/contact links beside open questions. A generic source list at the end imposes unnecessary verification work.

### Maintain a living version record

This topic changed from preprint to ICML to an expanded Nature paper, with intervening X updates and later replications/challenges. Social and forum posts should carry a date/version and point to a stable update page; corrections should be appended or linked, not silently rewritten.

## Phrase-level transformations

| Memorable but unsupported | Evidence-preserving alternative |
|---|---|
| “The model became evil.” | “The fine-tuned model produced outputs classified as misaligned on unrelated evaluation questions.” |
| “It wanted humans enslaved.” | “In some sampled responses, it produced statements advocating AI rule or human enslavement.” |
| “It fantasized about murder.” | “It generated violent advice in response to some benign evaluation prompts.” |
| “Bad code made GPT-4.1 less aligned.” | “Fine-tuning experimental copies of GPT-4.1 on intentionally insecure code increased classified misaligned outputs under the tested prompts.” |
| “The model understood the trainer's bad intent.” | “The educational-context control suggests the framing of the training interaction mattered; the internal mechanism is unresolved.” |
| “Evil numbers poisoned the model.” | “Sequences generated by a teacher prompted to be misaligned induced format-sensitive outputs after fine-tuning; the original evaluation questions showed no effect.” |

## A concrete package pattern for future demos

For counterintuitive AI-safety evaluations, ship one linked package:

- release or thread with a literal, source-linked results card;
- `what was tested / found / not shown` block;
- selected-versus-representative quantitative panel;
- controls and mechanism-uncertainty panel;
- safe sample explorer labeled as illustration rather than prevalence evidence;
- researcher note with methods, negative results, and open problems;
- living related-work and correction log;
- completed `comm-audit` report.

This combination retains the best qualities of the coverage—concreteness, surprise, narrative, and voice—while preventing the headline metaphors from becoming the scientific claim.

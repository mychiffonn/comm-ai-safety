# Press principles and AI pitfalls

Use this reference before choosing an angle and during adversarial editorial review.

## Press-release standard

A release is an interested institutional source. Make that status explicit and make independent verification easy.

- Put paper status, study/evaluation type, evaluated system, and evaluator relationship above or near the headline.
- State who evaluated what, under which interpretation-changing conditions, against what baseline, and with what result.
- Place the strongest limitation near the result; do not reserve it for the last paragraph.
- Separate observed result, author interpretation, institutional position, forecast, and recommendation.
- Disclose funding, employment, commissioning, provider support, access constraints, patents/equity/advisory roles, and review rights.
- Do not call work independent merely because the evaluator is outside the developer. Describe the actual relationship.
- Suggest independent experts only after checking subject fit and conflicts. Never imply availability or endorsement.
- Preserve human labor, supervision, data work, tools, and scaffolding that make the result possible.
- Treat quotes as evidence-bearing attributed speech: never invent them, label drafts, obtain speaker approval, and retain meaning through edits.

## News and comparison checks

- Define the news value without promotional adjectives.
- Verify “first,” “unprecedented,” “breakthrough,” “state of the art,” “human-level,” “expert-level,” “safer,” or “more dangerous” against a scoped and methodologically valid comparison.
- Match human/system comparisons on task, inputs, tools, time, scoring, sampling, and expertise. Otherwise describe differences rather than a contest.
- Include relevant prior and later work, contradictory findings, known replications, and stated future work. If no literature search was performed, say so.
- Do not turn a proposed experiment, announced product, forecast, or hypothetical threat path into a present result.
- Distinguish demonstrated capability from likelihood of access, deployment, misuse, or harm. The latter need a threat model, actor incentives, safeguards, and real-world evidence.

## Evidence-preserving storytelling patterns

Patterns repeatedly useful in careful coverage of counterintuitive AI evaluation results include:

- Open with `intervention → observed output shift → exact evaluation frame`; do not open with a mental-state verdict.
- Pair the headline number with its baseline in the same sentence, then state whether the questions or examples were selected, preregistered, or representative.
- Use one vivid output to make the result concrete, immediately followed by its frequency and selection status.
- Put the strongest control or negative result near the central claim. Controls are part of the story, not appendix debris.
- Make an unresolved mechanism an honest source of tension: “the study found X; it does not yet explain why.”
- Use a short plain-English label, then define the paper's operational meaning. Do not let a catchy term inherit broader everyday meanings.
- Place “what this does not show” before forecasts and policy implications.
- End with paper, data/code, an inspectable sample or demo when safe, current replications/challenges, and a correction contact.

For independent expert context, seek a technically relevant comment that tests the main inference, not a generic endorsement or a quote that merely repeats the authors. State the expert's relationship to the field and any relevant conflict.

Headline verbs should describe training, testing, or outputs—such as “fine-tuning changed sampled responses”—rather than minds or stable character. Wordplay can work when the literal subhead and lede promptly restore the experimental frame; a body paragraph cannot rescue a headline that asserts an unsupported mental state.

Researcher-authored X threads and LessWrong/Alignment Forum posts are useful source leads and can reveal controls, negative results, and uncertainty that a release should surface. Treat them as interested, versioned communication rather than independent validation, and verify technical claims against the paper or repository.

## Normal Technology's 18-pitfall audit

Test all pitfalls adapted from Kapoor and Narayanan's [“Eighteen pitfalls to beware of in AI journalism”](https://www.normaltech.ai/p/eighteen-pitfalls-to-beware-of-in):

1. Attributing independent agency.
2. Using suggestive robot imagery.
3. Making unsupported human-intelligence comparisons.
4. Making unfair human-skill comparisons.
5. Using hyperbole.
6. Invoking historical transformations without evidence.
7. Claiming unjustified future progress or inevitability.
8. Making false claims about what a system can do.
9. Misstating what the study reports.
10. Using deep-sounding language for ordinary operations.
11. Treating interested parties as neutral.
12. Repeating promotional terminology as technical fact.
13. Omitting limitations.
14. Burying or structurally minimizing limitations.
15. Framing evidence-based limitations as mere skepticism.
16. Hiding human labor and operational overhead.
17. Reporting performance without uncertainty, conditions, or caveats.
18. Using “black box” or inscrutability to avoid developer/deployer accountability.

For each triggered item, rewrite or record a justified exception. Review headlines, visuals, captions, quotes, and social derivatives separately; the body cannot repair a misleading headline.

## Sensitive-domain review

For bio/CBRN, cyber, autonomous weapons, critical infrastructure, self-proliferation, evasion, or sensitive vulnerabilities:

- do not add actionable operational detail absent from an already approved public source;
- distinguish model-only performance from human misuse uplift and physical-world success;
- obtain qualified domain-safety review;
- record deliberate omissions and their rationale without reproducing the sensitive material;
- verify confidentiality and embargo authority rather than inventing an embargo.

## Target-platform policy gate

Check the current submission/distribution rules before calling materials ready. Record whether the platform permits AI-assisted text, images, or multimedia; what disclosure is required; and who owns the rights.

Current example as of July 18, 2026: [EurekAlert's release guidelines](https://www.eurekalert.org/releaseguidelines), updated July 1, 2026, state that AI-generated text, images, and multimedia are generally ineligible, with limited case-by-case exceptions and rights documentation. Never imply that an LLM-drafted release is EurekAlert-eligible without current written confirmation.

## Licensing and asset rights

Public availability is not a license. Track the paper/report, figures, dataset, code, images, video, and the new release separately.

- Preserve the exact license name/version and notices.
- Record title, author, source, license link, and modifications for reused Creative Commons material.
- Check `ND`, `NC`, and `SA` terms rather than assuming all CC licenses are equivalent.
- Do not imply author, publisher, or licensor endorsement.
- Label synthetic visuals and verify their rights and target-platform eligibility.

## Evidence base

- A peer-reviewed observational study found that exaggerated university releases were associated with exaggerated news coverage, without clear evidence of more pickup: [Sumner et al., BMJ (2014)](https://www.bmj.com/content/349/bmj.g7015.abstract).
- [Science Media Centre reporting guidelines](https://www.sciencemediacentre.org/wp-content/uploads/2012/09/10-best-practice-guidelines-for-science-and-health-reporting.pdf) emphasize source, study design, causality, absolute risk, limitations, and external context.
- The [National Association of Science Writers Code](https://www.nasw.org/page/nasw-code-ethics-member-conduct) addresses accuracy, source credentials, conflicts, and corrections.
- The [Society of Professional Journalists Code](https://www.spj.org/spj-code-of-ethics/) addresses independence, labeling advocacy, conflicts, and transparency.
- [AP's AI reporting guidance](https://www.ap.org/the-definitive-source/announcements/ai-guidance-terms-added-to-ap-stylebook/) advises against human characteristics and gendered pronouns for AI systems.
- The UK AI Security Institute explains why [elicitation conditions](https://www.aisi.gov.uk/blog/our-approach-to-ai-capability-elicitation) materially affect capability claims.
- [NIST AI 800-1, second public draft](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.800-1.ipd2.pdf) distinguishes model-only evaluation from human-plus-AI uplift studies; treat it as draft guidance.
- [Creative Commons guidance](https://creativecommons.org/reusing-cc-licensed-content/) explains attribution and modification notices.

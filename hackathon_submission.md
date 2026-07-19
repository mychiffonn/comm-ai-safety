# Hackathon submission

## 1. Project name

**comm-ai-safety - communicate AI safety research with evidence-preserving agent skills**

## 2. Project details and description

`comm-ai-safety` is an open, portable package of Agent Skills for turning technical AI-safety sources into accurate public communication. It addresses a recurring failure mode in the field: when research moves into press releases, explainers, social posts, visuals, and demos, the evaluation conditions, uncertainty, caveats, and source provenance that determine what a result means are often lost.

The package serves AI-safety researchers, lab and university communications teams, journalists, and independent explainers. It provides three complementary skills:

- **`comm-public`** creates audience-specific explainers, FAQs, social copy, visual briefs, and safer demo briefs from primary sources.
- **`comm-press`** creates source-verifiable press releases, media briefs, pitches, and journalist FAQs.
- **`comm-audit`** audits any public-facing artifact against authoritative sources, checking claim fidelity, conditions, quantitative context, caveats, unsafe demo design, rights, and accessibility.

The package’s theory of change is concrete: users first build a source-anchored claim ledger; a responsible human validates it; the authoring skill adapts it to a named audience; and the audit skill checks the finished artifact before it is described as publishable. This makes it harder to confuse capability with propensity, benchmark results with real-world harm, or model behavior with human misuse uplift. It also leaves a reusable audit trail and reviewer record for future updates.

The repository includes a worked case study on _Emergent Misalignment_, with a version-aware source record, claim ledger, public-web coverage inventory, comparative audit, and writing-pattern analysis. The demo intentionally remains transparent about unverified or pending human-review items rather than claiming certainty it does not have.

## 3. Additional resources

- GitHub repository: https://github.com/chiffonng/comm-ai-safety
- Worked demo: [`demo/emergent-misalignment/`](demo/emergent-misalignment/)
- Pitch deck (PDF): [`outputs/comm-ai-safety-pitch.pdf`](outputs/comm-ai-safety-pitch.pdf)
- Pitch deck (PowerPoint): [`outputs/comm-ai-safety-pitch.pptx`](outputs/comm-ai-safety-pitch.pptx)

There is no separate demo video. The repository’s worked demo and pitch deck show the end-to-end workflow and concrete output.

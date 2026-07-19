# Emergent Misalignment communication demo

## 30-second overview

Researchers fine-tuned experimental versions of GPT-4o and GPT-4.1 on intentionally insecure code. Under specific evaluation prompts, the fine-tuned models produced more unrelated answers classified as misaligned than comparison models. The size of the effect varied substantially by model, prompt format, and evaluation set; the studies do **not** show that released models are routinely “evil,” have persistent goals, or caused real-world harm.

That is the demo's main message. The rest of this folder shows the evidence, boundaries, coverage context, and audit behind it.

This demo applies `comm-press` and `comm-audit` to two related but non-identical publications:

- the [February 2025 preprint](https://arxiv.org/abs/2502.17424) and [ICML 2025 proceedings paper](https://proceedings.mlr.press/v267/betley25a.html), *Emergent Misalignment: Narrow finetuning can produce broadly misaligned LLMs*;
- the expanded [January 2026 Nature paper](https://www.nature.com/articles/s41586-025-09937-5), *Training large language models on narrow tasks can lead to broad misalignment*.

The Nature paper adds GPT-4.1, prompt-format, training-dynamics, base-model, and follow-up results and adds an author. Coverage of the two waves must not be treated as coverage of an unchanged artifact.

## Files

- [`emergent-misalignment.md`](emergent-misalignment.md): standalone public-facing technical-report first draft based on the Nature article; Markdown was used because no other extension was requested.
- [`comm-press-run.md`](comm-press-run.md): Nature-only 30-second press brief, three takeaways, compact evidence map, verification queue, and workflow state.
- [`coverage-inventory.md`](coverage-inventory.md): deduplicated coverage located on the indexed public web, with source-family and inclusion notes.
- [`comm-audit-coverage.md`](comm-audit-coverage.md): comparative audit matrix, priority findings, strengths, and readiness decision.
- [`writing-patterns.md`](writing-patterns.md): practices learned from press coverage, publisher and university releases, researcher X threads, and LessWrong/Alignment Forum posts.
- [`.provenance.md`](.provenance.md): search protocol, source roles, access limits, and research-tool fallback.

## Current status

The `comm-press` run stops after producing the standalone Nature-only [`emergent-misalignment.md`](emergent-misalignment.md) so a writer can understand and react to concrete copy. Its three-point evidence map has received only the skill's initial source pass; full number verification, independent context, human approval, reader testing, and audit remain undone. Nothing in this folder is labeled final or publishable.

The independent corpus audit is complete as a **provisional, broad best-effort audit through July 18, 2026**. It covers every distinct editorial item located under the documented protocol, but some inaccessible, paywalled, translated, audio, or low-provenance items remain `unverified`. It does not claim globally exhaustive coverage.

## Continue the workflow

Continue with the `Verify next` queue in [`comm-press-run.md`](comm-press-run.md), then revise the concrete copy, obtain responsible-human approval, run a representative-reader test, and invoke the full `comm-audit` before publication.

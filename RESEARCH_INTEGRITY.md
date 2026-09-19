# Research Integrity and Reproducibility Rules

## Scope
This repository supports a research project on the use of artificial intelligence and natural language processing (NLP) for identifying misconceptions in middle-school science education.

## Non-negotiable rules

1. **Human annotation is the reference standard.** Model output, including large-language-model output, is never treated as ground truth.
2. **Empirical and synthetic data are separate.** Real participant responses must not be stored with synthetic/demo fixtures or mixed in the same evaluation split.
3. **No fabricated evidence.** The project must not invent participants, sample sizes, citations, scores, model results, or effectiveness claims.
4. **Auditable provenance.** Every dataset item, preprocessing configuration, model version, prompt/template, threshold, and evaluation run must have a stable identifier or manifest entry.
5. **Leakage prevention.** Splits are created by source/participant/item group before augmentation. Near-duplicates and augmented variants must not cross train/validation/test boundaries.
6. **Turkish language care.** Unicode normalization, Turkish casing, punctuation handling, tokenization, negation preservation, and optional stemming/lemmatization are explicit and testable.
7. **Evidence-linked explanations.** Explanations must point to spans in the original student response and may not manufacture rationales.
8. **Privacy and ethics.** Student data must be anonymized. Consent, institutional permissions, and ethics review must be documented before empirical analysis.
9. **Reproducibility.** Seeds, dataset versions, software versions, and experiment configurations are recorded.
10. **Transparent evaluation.** Report macro-F1, class-level precision/recall/F1, MCC, confusion matrices, calibration/error analysis, and uncertainty intervals where appropriate; accuracy alone is insufficient.
11. **No bypassing quality gates.** Failing tests, security checks, branch protection, or research-integrity checks must not be bypassed.
12. **Human review for uncertainty.** Low-confidence, contradictory, or out-of-taxonomy cases are routed to expert review.

## Data states

- `empirical`: de-identified data collected under the approved protocol.
- `synthetic`: generated or hand-written fixtures used only for tests and demos.
- `derived`: outputs created from empirical data by a documented pipeline.
- `restricted`: real data that must not be committed to a public repository.

## Merge policy

Each research phase must accumulate more than 3,000 substantive words of thesis/research documentation before the phase is considered complete. Individual pull requests must remain at or below 3,000 textual words. Large phases must be split into multiple reviewable pull requests. A merge is allowed only when all checks pass and no empirical claim is made without empirical evidence.

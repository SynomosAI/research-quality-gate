# research-quality-gate · Research Quality Gate

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.md)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-SKILL.md-blue.svg)](SKILL.md)
[![LLM-as-Judge](https://img.shields.io/badge/LLM-as--judge-5--dim-brightgreen.svg)](SKILL.md)

SynomosAI four-pillar system: **Identity · Traceability · Governance · Symbiosis**.

> This repo is part of the [SynomosAI](https://github.com/SynomosAI) skill ecosystem.

**Keywords**: research quality gate · evidence card · LLM-as-judge scoring · atomic-claim decomposition · multi-agent collaboration · PDCA · calibration

A quality gate for research / intelligence products: a 6-grid evidence-card check, a 5-dimension LLM-as-Judge score (with atomic-claim decomposition and bias control), and a multi-agent collaboration protocol. Embedded in the PDCA cycle since v1.3, aligned with ISO 9001 / 14001 / 27001 / 17025.

## Quick Start

Prerequisite: place this directory in your agent skills folder. No runtime dependencies.

```bash
git clone https://github.com/SynomosAI/research-quality-gate.git
cd research-quality-gate
cat SKILL.md
cat calibration-log.md
```

```text
Triggers: research quality gate · report plausibility check · 6-grid evidence card
expert-team collaboration · ISO 5725 stability · PDCA research framework
```

## What it covers

- **6-grid evidence card**: evidence grade (GRADE) · ICD 203 likelihood phrases · source summary (SIFT) · alternative hypotheses (triangulation) · delta vs prior judgment · provenance package.
- **5-dim LLM-as-Judge**: factual accuracy (FActScore atomic claims) · citation precision (NLI) · completeness · source quality · tool efficiency, with bias control (randomized order, cross-model judges, independent scoring).
- **Scope-boundary check**: before any evaluation, lock the agreed scope; out-of-scope omits are not failures.
- **Reproducibility threshold**: cross-judge Cohen's κ ≥ 0.4, else re-review / human escalation.

## Example (6-grid card excerpt)

```text
Claim: "X market penetration ~60% in 2026"
  1 evidence grade: moderate (downgraded for imprecision)
  2 likelihood: highly likely (80-95%, ICD 203)
  3 sources: one primary report + secondary press, strengths noted
  4 alternative: if "users" includes free tier, paid penetration may be 35%
  5 delta: 52% last quarter, +8pct
  6 provenance: URL + fetch time + snapshot archived
```

## License

MIT License. © 2026 注册老炮@MedXpert. See [LICENSE.md](LICENSE.md).

## Disclaimer

Theoretical-positioning and tooling exploration. External standards (ISO 9001/14001/27001/17025/20252, GRADE, FActScore) are paraphrased from public sources; verify independently before formal citation.

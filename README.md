# FDA Warning Letters — PAC Analysis

---

## Overview

This repository contains the violation-level coding dataset and analysis scripts used in:

> Kim, S. (2026). *Premature Accountability Convergence: Documentary Form, Computational Mediation, and the Temporal Architecture of Responsibility in Regulated Organizations.* SSRN Preprint.

The dataset consists of 160 violation observations extracted from 50 FDA Warning Letters issued to finished pharmaceutical drug product manufacturers between 2016 and 2025 (5 cases per year, purposive sampling). The analysis examines how attribution language varies across violation types while final accountability converges uniformly onto the regulated firm — establishing an empirical baseline for the PAC framework.

---

## Repository Contents

| File | Description |
|------|-------------|
| `FDA_Warning Letter.xlsx` | Original violation-level dataset (CaseID, ViolationID, CFR, ResponsibilitySubject, ViolationText) |
| `fda_warning_letters_coded.xlsx` | Coded dataset with AttributionLanguage classification (action / state / other) |
| `fda_attribution_coding.py` | Rule-based attribution language classification script and distribution analysis |

---

## Dataset

**Sampling:** 50 FDA Warning Letters issued to finished pharmaceutical drug product manufacturers (21 CFR 210/211), sampled at 5 cases per year across 2016–2025.

**Unit of analysis:** Violation block — individual observation or citation within each Warning Letter.

**Variables:**

| Variable | Description |
|----------|-------------|
| `CaseID` | Warning Letter identifier (e.g., WL2016-01) |
| `ViolationID` | Violation block identifier within case (e.g., V1, V2) |
| `CFR` | Cited regulatory provision (21 CFR) |
| `ResponsibilitySubject` | Attribution target (Firm / QualityControlUnit) |
| `ViolationText` | Researcher-coded violation description label |
| `AttributionLanguage` | Rule-based classification: action / state / other |

---

## Key Findings

- **159 of 160 violations** attribute responsibility to the Firm regardless of attribution language
- **Attribution language distribution:** state 66.2% · action 24.4% · other 9.4%
- Documentary form compresses causally heterogeneous violation descriptions into uniform Firm-level attribution — establishing a pre-computational baseline for PAC

---

## Attribution Language Classification

Rule-based classification applied to `ViolationText`:

- **action** — "failure to", "failed to", "failure of"
- **state** — "inadequate", "lack of", "incomplete", "insufficient", "absence of", "missing", "fabrication of"
- **other** — all remaining formulations

Full classification logic available in `fda_attribution_coding.py`.

---

## Related Work

This dataset supports the empirical illustration component of the PAC framework. For the broader research program on responsibility structuring in regulated sociotechnical systems, see:

- [Anticipated Accountability Convergence (AAC)](https://ssrn.com) — SSRN Preprint
- [Cognitive Friction in Procedural Texts (CF)](https://github.com/sorakim-phd/sop-cognitive-friction-pilot) — GitHub
- [Responsibility Convergence in Organizational Investigations (RC)](https://ssrn.com) — SSRN Preprint

---

## Citation

```
Kim, S. (2026). Premature Accountability Convergence: Documentary Form, Computational
Mediation, and the Temporal Architecture of Responsibility in Regulated Organizations.
SSRN Preprint.
```

---

*This repository is intended as a transparent research prototype demonstrating empirical patterns of responsibility convergence in FDA regulatory documentation, rather than a predictive or production-level system.*

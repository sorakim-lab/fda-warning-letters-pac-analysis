# FDA Warning Letters — PAC Analysis

---

## Overview

This repository contains the violation-level coding dataset and analysis scripts used in:

> Kim, S. (2026). *Premature Accountability Convergence: How Technology Accelerates Responsibility Stabilization in Organizations.* SSRN Preprint.

The dataset consists of 160 violation observations extracted from 50 FDA Warning Letters issued to finished pharmaceutical drug product manufacturers between 2016 and 2025 (5 cases per year, purposive sampling). The analysis examines how attribution language varies across violation types while final accountability converges uniformly onto the regulated firm — establishing a pre-technological empirical baseline for the PAC framework.

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
- **Violation type analysis:** attribution language varies substantially across categories (manufacturing violations: 91% state-form; investigation violations: 67% action-form) — yet Firm-level attribution is invariant across all categories (100%)
- Documentary form compresses causally heterogeneous violation descriptions into uniform Firm-level attribution — establishing a pre-technological baseline for the PAC framework

---

## Attribution Language Classification

Rule-based classification applied to `ViolationText`:

- **action** — "failure to", "failed to", "failure of"
- **state** — "inadequate", "lack of", "incomplete", "insufficient", "absence of", "missing", "fabrication of"
- **other** — all remaining formulations

Full classification logic available in `fda_attribution_coding.py`.

---

## Related Work

This dataset supports the empirical grounding component of the PAC framework. For the broader research program on responsibility structuring in regulated sociotechnical systems, see:

- [Anticipated Accountability Convergence (AAC)](https://www.ssrn.com/abstract=6371980) — SSRN Preprint
- [Cognitive Friction in Procedural Texts (CF)](https://github.com/sorakim-phd/sop-cognitive-friction-pilot) — GitHub
- [Responsibility Convergence in Organizational Investigations (RC)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=ORSC-MS-2026-22511) — SSRN Preprint

---

## Citation

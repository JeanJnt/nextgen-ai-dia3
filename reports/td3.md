# TD 3 Report: Costing, System Selection and Industrial Decision

**Sub-group**: DIA 3  
**Course**: Next-Generation AI - Trustworthy Generative AI (ESILV S7)  
**Session Date**: 2026-12-11  
**Pack Version**: `2026-10-14-students-1`  

---

## 1. Objectives & Scope

TD 3 finalizes the comparative analysis by:
- Quantifying token consumption and operational costs across single-model, quorum, and routed architectures.
- Justifying an architectural selection for a designated production use case based on cost-of-error impact.
- Presenting empirical findings, limitations, and reproducible evidence.

---

## 2. Configuration Analysis & Financial Modeling

- Comparative evaluation of single-model baseline, multi-model quorum ($k$-of-$n$), and dynamic routing.
- Token accounting based on empirical trace measurements and public API price indexes.
- Error mitigation rate versus inference expenditure.

---

## 3. Selected Use Case & Architecture Recommendation

- Use case description, operational constraints, and acceptable failure probability.
- Selected configuration architecture, justified by risk mitigation metrics.
- Projected operational expenses and fallback procedures.

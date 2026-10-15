# TD 2 Report: Quorum Voting and Routing Policy

**Sub-group**: DIA 3  
**Course**: Next-Generation AI - Trustworthy Generative AI (ESILV S7)  
**Session Date**: 2026-11-18  
**Pack Version**: `2026-10-14-students-1`  

---

## 1. Objectives & Scope

TD 2 implements and evaluates:
- A $k$-of-$n$ majority quorum mechanism within `skeleton-multi-llm-en.py`.
- Analysis of consensus behaviors, disagreement handling, and identification of false consensus occurrences.
- Development and empirical testing of a production routing rule based on difficulty, latency, and cost trade-offs.

---

## 2. Quorum Implementation & Threshold Testing

- **Panel Selection**: Three complementary model families evaluated in parallel.
- **Vote Algorithm**: Extraction and normalization of SQL execution results, majority detection, and abstention rules.
- **Validation**: Test coverage across synthetic test cases (`atelier-vote.py`) and historical TD 1 execution traces.

---

## 3. False Consensus Analysis

- Detailed breakdown of identical errors produced by distinct model architectures.
- Root causes: shared training biases, ambiguous prompt semantics, or common SQL syntax pitfalls.

---

## 4. Sub-group Routing Rule

- Routing policy definition linking query complexity categories to the lowest-cost capable model.
- Evaluation across the seven operational scenarios of `atelier-routage.py`.

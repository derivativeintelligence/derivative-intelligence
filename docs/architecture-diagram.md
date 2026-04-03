# DI System Architecture Diagram

---

This diagram represents the full execution flow of a Derivative Intelligence (DI) system.

It illustrates how probabilistic model generation is transformed into governed, explainable, and auditable system behavior.

---

## Diagram

![DI System Architecture](../assets/di-system-architecture.png)

---

## Flow Summary

User Input  
→ Context Builder  
→ Model Layer (Derivative Engine)  
→ Policy Engine (Corpus-aligned)  
→ Decision Engine  
→ Explanation Layer  
→ Output  
→ Audit & Logging  

---

## Key Layers

### Model Layer (Generation)

- produces candidate outputs  
- probabilistic by nature  
- derived from human knowledge  

---

### Policy Engine (Control)

- enforces corpus-aligned constraints  
- evaluates outputs deterministically  
- prevents violations and non-compliant behavior  

---

### Decision Engine (Selection)

- ranks candidate outputs  
- applies policy scoring  
- selects final response  

---

### Explanation Layer (Transparency)

- explains why a decision was made  
- identifies data sources used  
- communicates expected outcomes  

---

### Audit & Logging (Accountability)

- records full system activity  
- enables traceability and verification  
- supports optional on-chain anchoring  

---

## Underlying Data Layer

All system components operate on a structured data foundation:

- Foundational Corpus (immutable)  
- Interpretation Corpus (governed)  
- External Knowledge (dynamic)  
- Human Evaluation Data (feedback)  

Each data class remains explicitly separated and traceable.

---

## Governance Layer

System behavior evolves through governance, not hidden updates.

- proposal-based changes  
- transparent review and approval  
- policy and interpretation updates  
- optional on-chain verification  

---

## Core Insight

The model generates.  
The policy governs.  
The system explains.

---

## Mental Model

DATA → MODEL → POLICY → DECISION → EXPLANATION → AUDIT
↑          ↓
(probabilistic) (deterministic)

---

## Why This Matters

Traditional AI systems are:

- opaque  
- centrally controlled  
- difficult to audit  

DI systems are:

- transparent by design  
- governed by principles  
- verifiable and auditable  

---

## Summary

This architecture ensures that:

- outputs are not just generated, but governed  
- reasoning is not hidden, but exposed  
- system behavior is not arbitrary, but principled  

---

## Final Statement

Machines derive.  
Humans originate.

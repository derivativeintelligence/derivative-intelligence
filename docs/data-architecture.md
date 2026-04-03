# Data Architecture: Derivative Intelligence Systems

---

## Overview

This document defines the data architecture required to support Derivative Intelligence (DI) systems.

The architecture is designed to:

- enforce separation of concerns  
- preserve data integrity and provenance  
- enable transparency and auditability  
- support principle-aligned system behavior  

This structure is a direct consequence of the foundational corpus:

→ `/docs/corpus-v0.1.md`

---

## Design Principles

The data architecture follows these core principles:

- **Separation**: Different classes of knowledge must remain distinct  
- **Traceability**: All data must have identifiable origin and lineage  
- **Verifiability**: Critical artifacts must be cryptographically provable  
- **Governance**: Changes must follow explicit processes  
- **Non-Deception**: Systems must not conflate source types  

---

## Data Classification

All data in a DI system is organized into four primary classes.

---

## Class 1: Foundational Corpus (Immutable)

### Description

The foundational corpus represents the **constitutional layer** of the system.

It contains the primary source material that defines the system’s grounding.

---

### Examples

- canonical source texts  
- authoritative reference documents  
- foundational principles (e.g. corpus-v0.1)  
- canonical identifiers and metadata  

---

### Properties

- immutable once published  
- version-controlled  
- globally identifiable  
- cryptographically hashed  

---

### Storage Model

- stored off-chain for accessibility  
- hashed and anchored on-chain for integrity  

---

### Constraints

- cannot be modified directly  
- can only be superseded through governed version updates  

---

### Purpose

- defines system boundaries  
- anchors interpretation  
- ensures long-term stability  

---

## Class 2: Interpretation Corpus (Governed)

### Description

The interpretation corpus contains **contextual and analytical layers** applied to the foundational corpus.

It represents human understanding evolving over time.

---

### Examples

- scholarly commentary  
- interpretive frameworks  
- domain-specific analysis  
- multi-perspective reasoning  

---

### Properties

- versioned  
- attributed to source (author, institution, era)  
- labeled with metadata such as:
  - perspective or school of thought  
  - confidence level  
  - methodological approach  

---

### Storage Model

- stored off-chain  
- optionally hash-anchored for version integrity  

---

### Governance

- updated via proposal process  
- subject to review and discussion  
- cannot override the foundational corpus  

---

### Purpose

- provides context and depth  
- enables multiple perspectives  
- supports reasoning and explanation  

---

## Class 3: External Knowledge (Dynamic)

### Description

This class includes all **non-foundational, evolving knowledge sources**.

It represents the system’s connection to the broader world.

---

### Examples

- scientific research  
- educational content  
- encyclopedic data  
- legal and regulatory materials  
- real-time data inputs  

---

### Properties

- continuously updated  
- not inherently authoritative  
- variable reliability  

---

### Storage Model

- stored off-chain  
- selected snapshots may be hash-anchored  

---

### Constraints

- must be clearly distinguished from foundational and interpretive data  
- must include source attribution and confidence indicators  

---

### Purpose

- enables adaptability  
- supports real-world reasoning  
- expands system capability  

---

## Class 4: Human Evaluation Data (Feedback Layer)

### Description

This class captures **human judgment and evaluation signals** used to improve system performance.

---

### Examples

- expert evaluations  
- ranking and preference data  
- output quality assessments  
- consistency reviews  
- safety and alignment labels  

---

### Properties

- subjective but structured  
- continuously evolving  
- dependent on contributor expertise  

---

### Storage Model

- stored off-chain  
- versioned and attributed  

---

### Usage

- training reinforcement models (RLHF / RLAIF)  
- improving ranking and decision-making  
- refining alignment behavior  

---

### Constraints

- must not override foundational principles  
- must be interpreted within governance framework  

---

## Data Flow Model

```text
Foundational Corpus
        ↓
Interpretation Corpus
        ↓
External Knowledge
        ↓
Model Generation
        ↓
Policy Engine (Corpus-aligned)
        ↓
Decision Output
        ↓
Human Evaluation Feedback

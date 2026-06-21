**Chain of Truth (CoT)** is an AI-assisted software development workflow that uses **validated artifacts as the Source of Truth (SoT)** at every stage of development.

Chain of Truth builds a series of interconnected and validated artifacts, ranging from requirements, user flows, data models, to implementation and testing. Each artifact becomes the official reference for the next process.

With this approach, AI is still used to accelerate work, but development decisions are controlled by clear, traceable, and verifiable artifacts.

The main goal of Chain of Truth is to improve **traceability, consistency, reproducibility, and integration quality** in AI-assisted software development.

## Chain of Truth Phases

Chain of Truth consists of seven main phases that form a Source of Truth chain from idea to release-ready software.

![CoT Method](https://raw.githubusercontent.com/faridsurya-dev/public-images/refs/heads/main/Chain%20of%20Truth%20Software%20Dev%20Method-Page-1.drawio.png)

### 1. Software Requirements Specification (SRS)

[[Phase 1 - SRS Development]] translates product ideas, business needs, and user requirements into a structured requirements document.

The output of this phase is a **Validated SRS (SoT #1)** which becomes the foundation for all subsequent artifacts.

**Goal:** ensure the entire team has a shared understanding of what will be built.

### 2. Product Structure Development

In [[Phase 2 - Product Structure Development]], the SRS is broken down into three main artifacts:

- Information Architecture (IA)
- Design System
- User Flows

All three are developed and validated separately.

The outputs of this phase are:

- **Validated Information Architecture (SoT #2)**    
- **Validated Design System (SoT #3)**    
- **Validated User Flows (SoT #4)**    

**Goal:** define the product structure, user experience, and design rules before implementation begins.

### 3. High Fidelity Prototype Development

User Flow, IA, and Design System are used to generate a prototype that resembles the final product. These three SoTs are used for [[Phase 3 - High-Fidelity Prototype Development]].

The prototype is used to validate usage flows and user experience before coding begins.

The output of this phase is a **Validated HiFi Prototype (SoT #5)**.

**Goal:** validate design and system behavior early so the cost of change is lower.

### 4. Data Model Development

[[Phase 4 - Data Model Development]] produces a data model based on validated User Flows.

The Data Model defines:

- Entities    
- Attributes    
- Relationships    
- Business Rules    
- Validation Rules    

The output of this phase is a **Validated Data Model (SoT #6)**.

**Goal:** ensure the data structure supports all business processes defined in the User Flows.

### 5. Use Case Integration Contract (UCIC) Development

[[Phase 5 - Use Case Integration Contract (UCIC) Development]] is the phase for developing system integration artifacts. UCIC is an integration contract at the use case level that aligns frontend, backend, API, and testing.

Each UCIC defines:

- Sequence Diagram    
- API Contract    
- Request & Response Structure    
- Validation Rules    
- Error Handling    

The output of this phase is a **Validated UCIC (SoT #7)**.

**Goal:** eliminate different assumptions between frontend and backend before implementation begins.

### 6. Implementation

[[Phase 6 - Implementation]] transforms all Sources of Truth into running software.

- Frontend is built based on HiFi Prototype and UCIC.    
- Backend is built based on Data Model and UCIC.    
- Integration is done according to agreed contracts.    

**Goal:** ensure implementation follows validated artifacts, not individual developer interpretations.

### 7. Testing

[[Phase 7 - Testing and Validation]] verifies that the implementation conforms to all Sources of Truth.

Testing is created based on:

- User Flows    
- UCIC    
- Acceptance Criteria    

If issues are found, fixes are made to the artifact that is the source of the problem, not by directly patching the code.

**Goal:** ensure the resulting software truly meets user needs and agreed specifications.

## Source of Truth Chain

```text
SRS
 ↓
Information Architecture
Design System
User Flows
 ↓
HiFi Prototype
 ↓
Data Model
 ↓
Use Case Integration Contract
 ↓
Implementation
 ↓
Testing
```

Each phase produces validated artifacts that become the **Source of Truth** for the next phase. This way, changes can be traced, decisions can be audited, and AI can work with clearer and more consistent context.

## Publication

The academic article version of this workflow can be accessed through the following preprint repository:

```
Suryanto, F., & Ibnu, A. (2026). Chain of Truth: A Source-of-Truth Workflow for AI-Assisted Software Development. Zenodo. https://doi.org/10.5281/zenodo.20767965
```

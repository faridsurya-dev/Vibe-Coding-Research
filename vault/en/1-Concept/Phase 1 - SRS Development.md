## What is SRS?

Software Requirements Specification (SRS) is a document that defines software requirements in a structured, complete, and verifiable manner.

SRS is not a new concept that emerged because of AI or the Chain of Truth method. SRS is an artifact that has long been used in the Software Engineering discipline and has standards published by the **Institute of Electrical and Electronics Engineers (IEEE)** through the **IEEE Recommended Practice for Software Requirements Specifications (IEEE 830)** standard, later updated in **ISO/IEC/IEEE 29148** for Requirements Engineering.

The main goal of SRS is to transform business needs, user requirements, and product goals into clear specifications that can be understood, implemented, tested, and maintained by the development team.

In modern practice, the SRS format does not have to strictly follow the IEEE template. Many organizations use lighter versions according to project needs. However, the basic principles remain the same:

- Requirements must be explicit.
- Requirements must be verifiable.
- Requirements must be traceable.
- Requirements must be the basis for design, implementation, and testing.

In Chain of Truth, SRS serves as the **first Source of Truth (SoT #1)**. SRS is the starting point that transforms product ideas into software engineering artifacts that can be used to generate User Flows, Information Architecture, Design System, Data Model, and other artifacts.

### SRS vs PRD

Many people use the terms PRD (Product Requirements Document) and SRS (Software Requirements Specification) interchangeably. However, they have different focuses.

|Aspect|PRD|SRS|
|---|---|---|
|Focus|Product|Software System|
|Goal|Explain what to build and why|Explain in detail how system requirements are defined|
|Primary Audience|Product Manager, Business Stakeholder|Developer, Architect, QA, AI Coding Assistant|
|Main Content|Problem, Vision, User Needs, Success Metrics|Functional Requirements, Non-Functional Requirements, Business Rules, Constraints|
|Detail Level|Medium|High|
|Orientation|Business and Product|Engineering and Implementation|

Simply put, **PRD answers:** _"What product do we want to build and why?"_. While **SRS answers:** _"What software requirements must be fulfilled to realize that product?"_

## The Role of SRS in Development

SRS serves as the foundation of software development.

1. Align Understanding: SRS ensures all stakeholders have the same understanding of product goals, scope, user needs, and features to be built.

2. Reduce Ambiguity: Many project failures come from unclear requirements that only exist in conversations. SRS turns those requirements into explicit and documented specifications.

3. Serve as Development Reference: All downstream artifacts are built upon the validated SRS. Thus, AI and developers do not work based on assumptions or personal interpretations.

4. Support Traceability: Every User Flow, Data Model, API Contract, implementation, and test case can be traced back to its underlying requirement.

5. Control Change: When requirements change, the team can update the SRS first, then propagate those changes to other artifacts systematically.

## How to Build SRS

The main goal of this phase is to transform product ideas into clear requirements that can be used as a development foundation.

### Step 1 — Understand the Problem

Gather information from:

- Product vision    
- Business goals    
- Stakeholder interviews    
- User research    
- Existing processes    
- Technical constraints    

Focus on these questions:

- What problem needs to be solved?    
- Who are the system users?    
- What value do we want to deliver?    
- What constraints must be followed?    

### Step 2 — Define Scope

Determine:

- In Scope    
- Out of Scope    
- Assumptions    
- Constraints    

This stage is important to prevent scope creep from the beginning.

### Step 3 — Identify Actors and Goals

For each user type:

- Who are they?    
- What are their goals?    
- What activities do they want to perform?    

The output of this stage is typically a list of user roles and user goals.

### Step 4 — Define Features

Each feature is described in terms of:

- Feature name    
- Description    
- Functional requirements    
- Business rules    

Example:

**Feature: Account Registration**

Requirements:

- The system must allow users to create an account.    
- The system must verify the user's email.    
- The system must reject already registered emails.    

### Step 5 — Define Non-Functional Requirements

Examples:

- Performance    
- Security    
- Availability    
- Scalability    
- Maintainability    
- Usability    

Non-functional requirements are often a source of problems if not defined from the start.

### Step 6 — Review and Validate

SRS is not yet a Source of Truth until validated.

Validation is done to ensure:

- Requirements are correct    
- Requirements are complete    
- Scope is appropriate    
- No contradictions    
- Can be implemented    

Once approved by stakeholders, the document's status changes to **Validated SRS (SoT #1)** and can be used to produce subsequent artifacts.

## SRS Structure

The SRS structure used in Chain of Truth is kept lightweight so it can be easily used by both humans and AI.

### 1. Introduction

Contains:

- Purpose    
- Scope    
- Stakeholders    
- Definitions    
- References    

### 2. Product Overview

Contains:

- Product Summary    
- User Types    
- User Goals    
- Operating Environment    
- Assumptions    
- Constraints    

### 3. System Features

For each feature:

- Feature ID    
- Feature Name    
- Description    
- Functional Requirements    
- Business Rules    

### 4. Data Requirements

Contains:

- Core Business Objects    
- Ownership Rules    
- Data Retention Rules    
- Data Validation Rules    

### 5. External Interfaces

Contains:

- UI Requirements    
- External Systems    
- Communication Requirements    

### 6. Non-Functional Requirements

Contains:

- Performance    
- Security    
- Availability    
- Reliability    
- Scalability    
- Maintainability    
- Usability    

### 7. Permissions and Access Control

Explains access rights for each role.

### 8. Feature Inventory

List of all features and their priorities.

### 9. Open Questions

Items that still need clarification.

### 10. Future Considerations

Ideas or requirements not yet in the current scope.

### 11. Revision History

Document change history to maintain traceability.

**Output of SRS Development Phase:**  
**Validated SRS (Source of Truth #1)** which serves as the basis for creating Information Architecture, Design System, and User Flows in subsequent phases of Chain of Truth.

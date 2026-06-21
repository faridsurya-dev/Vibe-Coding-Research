# Chain of Truth in Practice #1

## Building a Frontend Web Application from Source of Truth

> **With Chain of Truth, AI no longer depends on prompts. It depends on Source of Truth.**

## 🚀 Try It Yourself

This implementation case study is fully reproducible.

Source of Truth artifacts used in this experiment are available here:

Repository:
https://github.com/faridsurya-dev/vibe_coding_simple_case

You can inspect the documents, use them with your preferred AI coding assistant, and compare the results yourself. The image below is the result using Bigpickle model, an opersource model accessed with opencode.

![cahsier app](https://raw.githubusercontent.com/faridsurya-dev/public-images/refs/heads/main/Screenshot%202026-06-21%20133741.png)

# Introduction

One of the biggest challenges in AI-assisted software development is consistency.

Most vibe coding workflows rely heavily on prompts. Requirements, business rules, UI decisions, and implementation details are gradually accumulated inside conversations.

This approach works well for small experiments, but problems emerge as projects grow:

* Requirements become scattered across chats.
* AI may interpret the same feature differently over time.
* Context is lost when starting a new session.
* Different models may produce different implementations.
* Validation becomes subjective.

Chain of Truth (CoT) was created to address this problem.

Instead of storing project knowledge inside prompts, CoT moves knowledge into structured artifacts called **Sources of Truth (SoT)**.

This case study demonstrates how CoT was used to build a complete frontend web application with dummy API integration while keeping prompts minimal and implementation consistent.

# Objective

The objective of this implementation was not to build a POS application.

The objective was to validate the following hypothesis:

> A sufficiently detailed Source of Truth can guide an AI coding assistant to implement an application without requiring feature-specific prompts.

The resulting application serves only as a vehicle to test the workflow.

# Project Overview

## Application

Web-Based Point of Sale (POS)

## Domain

Retail

## User Role

Cashier

## Main Features

### Sales Transaction

* Login
* Product browsing
* Cart management
* Checkout
* Receipt printing

### Inventory Management

* Add product
* Stock monitoring

### Reporting

* Daily sales report
* Monthly sales report

# Chain of Truth Workflow

The complete Chain of Truth workflow begins with an SRS.

```text
SRS
 ↓
Information Architecture
 ↓
Design System
 ↓
User Flows
 ↓
UCIC / System Logics
 ↓
Implementation
```

However, during implementation the coding assistant did not directly use the SRS.

The implementation phase consumed only the operational artifacts:

* Information Architecture
* Design System
* User Flows
* UCIC (System Logics)

These artifacts acted as the implementation-level Source of Truth.

# Source of Truth Artifacts

## 1. Information Architecture (IA)

The IA defines:

* Pages
* Navigation hierarchy
* Routing structure
* Relationships between screens

The IA answers:

> What pages exist in the application?

## 2. Design System

The Design System defines:

* Visual language
* Components
* Layout rules
* UI consistency standards

The Design System answers:

> How should the application look?

## 3. User Flows

User Flows define:

* User interactions
* Main flows
* Alternative flows
* Exception flows

User Flows answer:

> How should the application behave?

## 4. UCIC (System Logics)

UCIC defines:

* System behavior
* Interaction contracts
* Application logic
* API expectations

UCIC answers:

> What should happen behind the interface?

# Development Environment

## IDE

OpenCode

## Models

* Bigpickle
* DeepSeek V4 Flash

## Session Strategy

Single session.

The entire implementation was completed within a single development session.

# The Prompts

One of the most surprising results of this experiment was the simplicity of the prompts.

Only three user prompts were used.

## Prompt 1

```text
Create a blank starter app using latest nextjs in 'pos_simple_[model_name]' folder.
```

## Prompt 2

```text
Based on @docs/design_system.md and @docs/information_architecture.md, create the application's pages and navigations structure.
```

## Prompt 3

```text
Implement the application's functionality in detail based on docs/user_flows/* and docs/system_logics/*, using dummy API calls where needed.
```

Notice what is missing.

The prompts do not contain:

* business requirements
* feature descriptions
* validation rules
* UI specifications
* application logic

Those details already exist inside the Source of Truth.

The prompts merely instruct the AI to execute.

# From Prompt-Driven Development to Source-of-Truth-Driven Development

Traditional vibe coding often looks like this:

```text
Requirement
 ↓
Prompt
 ↓
AI
 ↓
Prompt Revision
 ↓
AI
 ↓
More Prompts
 ↓
AI
```

Over time, project knowledge becomes distributed across conversations.

Chain of Truth changes the workflow:

```text
Requirement
 ↓
Source of Truth
 ↓
AI
```

The Source of Truth becomes the carrier of knowledge.

Prompts become execution instructions.

This shift is the core idea behind Chain of Truth.

# Development Results

The AI coding assistant successfully generated:

* Complete frontend application
* Application navigation
* UI screens
* User interactions
* Dummy API integration
* End-to-end workflows

The resulting application was fully navigable and functional within the defined scope.

# Human Intervention

An important observation during the experiment was the nature of user intervention.

Additional messages were required only when technical execution issues occurred, such as:

* file generation failures
* temporary model access issues
* connectivity interruptions

The fixes consisted of simply copying and pasting error messages.

No additional prompts were needed to explain:

* features
* business rules
* workflows
* validation requirements

This indicates that the Source of Truth provided sufficient implementation context.

# Validation Strategy

Validation was not performed through visual inspection alone.

Instead, test cases were derived from:

```text
SRS
 ↓
User Flows
 ↓
Test Cases
```

This created an independent validation layer.

The implementation was evaluated against predefined expectations rather than subjective judgment.

# Test Results

## Total Test Cases

30

## Passed

100% of applicable frontend test cases

## Failed

0

## Excluded

Test cases requiring a real backend implementation

The result demonstrates that the generated application was consistent with the requirements captured in the Source of Truth.

# Key Findings

## Finding #1 — The Biggest Benefit Was Consistency

The most significant benefit observed was not speed.

It was consistency.

Before Chain of Truth:

* requirements lived in conversations
* context drift occurred frequently
* feature implementations became inconsistent

After Chain of Truth:

* requirements lived in artifacts
* implementation became traceable
* context remained stable
* AI behavior became more predictable

## Finding #2 — Prompts Became Smaller

The reduction in prompt complexity was a side effect.

The real achievement was moving project knowledge out of prompts and into artifacts.

As a result:

* prompts became shorter
* sessions became reproducible
* models became interchangeable

## Finding #3 — Validation Became Objective

Without a Source of Truth:

```text
Does the application look correct?
```

With a Source of Truth:

```text
Does the implementation satisfy the test cases?
```

This is a fundamentally different validation model.

# Why This Matters

Many AI-assisted development workflows optimize prompts.

Chain of Truth optimizes context.

Prompt engineering attempts to improve communication with AI.

Chain of Truth attempts to improve the quality and structure of the knowledge provided to AI.

The distinction is subtle but important.

When context is reliable, prompts become simple.

When context is unreliable, prompt engineering becomes endless.

# Conclusion

This experiment demonstrates that a frontend web application can be implemented successfully using Chain of Truth with minimal prompting.

The coding assistant received only three execution-oriented prompts and relied on Source of Truth artifacts for all functional and behavioral decisions.

The resulting application:

* was fully navigable
* implemented the intended workflows
* integrated dummy APIs
* passed all applicable frontend test cases

Most importantly, the experiment showed that:

> **With Chain of Truth, AI no longer depends on prompts. It depends on Source of Truth.**

# Support the Research

Chain of Truth is an independent research initiative focused on improving AI-assisted software development.

If this work helps you, consider supporting future research and experiments:

https://saweria.co/faridsurya

Every contribution helps fund additional experiments, documentation, tooling, and open-source resources for the community.

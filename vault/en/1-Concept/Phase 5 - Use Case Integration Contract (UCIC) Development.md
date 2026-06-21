After User Flows and Data Model are validated, the next stage is to prepare the **Use Case Integration Contract (UCIC)**. This phase aims to translate business needs, user flows, and data structures into integration contracts that can be used jointly by frontend, backend, QA, and AI coding assistants.

In many projects, problems do not arise because of incorrect requirements, but because frontend and backend have different interpretations of the same requirement. The frontend expects a certain data format, while the backend returns a different format. The frontend considers a process only needs one API, while the backend splits it into multiple endpoints.

UCIC is created to eliminate these assumptions.

### What is UCIC?

UCIC is an implementation contract at the use case level.

If User Flow explains:

> What the user does.

And Data Model explains:

> What data the system uses.

Then UCIC explains:

> How frontend, backend, API, and database work together to realize that use case.

UCIC becomes the shared language used by the entire team before implementation begins.

### UCIC Inputs

UCIC is built from two main Sources of Truth:

- SoT #4 — Validated User Flows    
- SoT #6 — Validated Data Model    

```text
User Flow
      +
Data Model
      ↓
     UCIC
```

User Flow provides business process context, while Data Model provides the data structure context used during the process.

### What is Built?

Each use case has its own UCIC.

Minimum UCIC content includes:

- Use Case Reference    
- Related Screens    
- Related Entities    
- Sequence Diagram    
- API Contract    
- Request Payload    
- Response Payload    
- Status Codes    
- Validation Rules    
- Data Mapping    
- Error Handling    

With UCIC, all integration details are defined before frontend and backend development begins.

### Simple Example

Suppose there is a use case:

**UC-001 — Login**

User Flow explains:

```text
User enters email and password
↓
System verifies credentials
↓
System returns a token
↓
User enters the dashboard
```

UCIC then defines:

- Endpoint: POST /auth/login    
- Request Body    
- Response Body    
- Error Response    
- Input Validation    
- Sequence Diagram    
- Mapping to User entity    

Thus, frontend and backend have the same understanding of how that use case should be implemented.

### Why is UCIC Important?

Without a clear integration contract, frontend and backend often develop separately based on their own assumptions.

This results in problems such as:

- Endpoints do not match UI needs    
- Payload differs from expectations    
- Status codes are inconsistent    
- Error handling differs    
- Integration issues are discovered late    

UCIC reduces these risks by making integration a validated artifact before implementation begins.

### UCIC Validation

Before becoming a Source of Truth, UCIC needs to be reviewed to ensure:

- Supports all steps in the User Flow.    
- Uses the correct Data Model.    
- API Contract is complete.    
- Data Mapping is clear.    
- Error Handling is defined.    
- Frontend and backend have the same understanding.    

If discrepancies are found, revisions are made to the User Flow, Data Model, or UCIC according to the source of the problem.

### Output of Phase 5

This phase produces:

|Source of Truth|Description|
|---|---|
|SoT #7|Validated UCIC|

The validated UCIC becomes the main reference for:

- Frontend implementation    
- Backend implementation    
- API development    
- Frontend-backend integration    
- Contract testing    
- Integration testing    

### Key Principle of Phase 5

The focus of this phase is not building an API, but building an **integration agreement** before code is written.

With UCIC, frontend and backend no longer work based on their own interpretations, but based on the same contract. This makes implementation more consistent, reduces integration mismatches, and provides much clearer context for AI coding assistants when generating code.

After implementation is complete, the next stage is to ensure that the built software truly conforms to the needs defined across all Sources of Truth. This phase focuses on verification and validation of the system before the software is declared ready for release.

In Chain of Truth, testing is not only done against code. Testing is done against the conformance of the implementation with previously validated artifacts. Thus, the question to be answered is not just:

> "Does the code run?"

But:

> "Does the built system meet the agreed requirements?"

### Goals of the Testing Phase

The main goal of this phase is to ensure that:

- Requirements have been fulfilled.    
- User Flows work as designed.    
- APIs work according to contract.    
- Frontend and backend integration works correctly.    
- Error handling works as expected.    
- Acceptance criteria are met.    

This phase is the final gateway before the system can be considered ready for use.

### Basis for Test Case Development

In Chain of Truth, test cases are derived from Sources of Truth, not created based on code alone.

The main sources of testing are:

|Source of Truth|Used For|
|---|---|
|User Flows (SoT #4)|Functional Testing, User Journey Testing, Acceptance Testing|
|UCIC (SoT #7)|API Testing, Contract Testing, Integration Testing|
|HiFi Prototype (SoT #5)|UI Validation and User Acceptance Review|

This approach keeps testing focused on business needs and expected system behavior.

### Types of Testing

#### Functional Testing

Ensures each use case works according to User Flow.

Examples:

- Login succeeds.    
- Creating an order succeeds.    
- Canceling a transaction succeeds.    

#### API Testing

Ensures endpoints work according to the contract defined in UCIC.

Examples:

- Request payload is valid.    
- Response payload matches specification.    
- Status code is correct.    
- Error response follows contract.    

#### Integration Testing

Ensures frontend and backend can work together without integration issues.

Examples:

- Frontend form sends correct data.    
- Backend returns appropriate response.    
- Data is stored correctly in the database.    

#### Acceptance Testing

Ensures the system meets the acceptance criteria established in User Flows.

Acceptance Testing is usually performed by stakeholders or the product owner before the system is declared ready for use.

### When Testing Fails

One of the important principles in Chain of Truth is:

> Fix the artifact that causes the problem, not just the symptoms.

When a test failure is found, the team must determine the source of the problem:

#### If Implementation is Wrong

```text
Requirement is correct
↓
User Flow is correct
↓
UCIC is correct
↓
Implementation is wrong
```

Then the code implementation is what gets fixed.

#### If Source of Truth is Wrong

```text
Requirement is correct
↓
User Flow is incomplete
↓
UCIC becomes wrong
↓
Implementation follows UCIC
```

Then the User Flow is fixed, then its derivative artifacts are updated and re-validated.

This approach prevents undocumented patching practices and maintains consistency across the entire artifact chain.

### Output of Phase 7

If all testing is successfully passed, the output of this phase is:

- Validated System    
- Release Candidate    
- Test Results    
- Validation Records    

These artifacts serve as evidence that the implementation has met the requirements defined in the Sources of Truth.

### Key Principle of Phase 7

Testing is not merely a bug-finding activity. In Chain of Truth, testing is the process of verifying that the entire artifact chain — from requirements to implementation — remains consistent.

The success of this phase is not only measured by the number of bugs found, but by the team's ability to answer the question:

> Does the built system truly realize the user needs as defined in the Chain of Truth?

If the answer is yes, then the implementation result can be promoted to a **Release Candidate** and is ready to enter the deployment or release process.

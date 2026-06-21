After all main artifacts are validated, the next stage is to transform specifications into running software. In this phase, the team begins building frontend, backend, database, and integration based on the previously agreed Sources of Truth.

Unlike the prompt-to-code approach that often directly generates code from natural language instructions, in Chain of Truth implementation is done based on validated artifacts. Thus, AI and developers work using clear, documented, and traceable context.

### Goals of the Implementation Phase

The goal of this phase is not merely to produce code, but to ensure that the implementation conforms to the needs defined in previous phases.

Each part of the system has a clear reference source:

- Frontend refers to HiFi Prototype and UCIC.    
- Backend refers to Data Model and UCIC.    
- Integration refers to UCIC.    

With this approach, implementation becomes a process of translating Sources of Truth into code, not a process of reinterpreting requirements.

### Frontend Implementation

Frontend development uses two main artifacts:

- SoT #5 — Validated HiFi Prototype    
- SoT #7 — Validated UCIC    

Frontend is responsible for implementing:

- Pages and navigation    
- UI Components    
- Forms and validation    
- State management    
- API integration    
- Error handling    
- User interactions    

The HiFi Prototype serves as the reference for appearance and user experience, while UCIC serves as the reference for communication with the backend.

### Backend Implementation

Backend development uses:

- SoT #6 — Validated Data Model    
- SoT #7 — Validated UCIC    

Backend is responsible for implementing:

- Business logic    
- Database schema    
- API endpoints    
- Authentication and authorization    
- Validation rules    
- Data processing    
- Error responses    

The Data Model defines the data structure to be managed, while UCIC defines the API behavior that must be provided.

### Frontend-Backend Integration

After frontend and backend are developed, they are integrated using the contracts established in UCIC.

Because frontend and backend use the same reference, the risk of issues such as:

- Endpoint not found    
- Payload mismatch    
- Different response format    
- Inconsistent status codes    
- Unsynchronized error handling    

can be significantly reduced.

### The Role of AI in the Implementation Phase

AI can be used to help:

- Generate frontend code    
- Generate backend code    
- Generate database schema    
- Generate API implementation    
- Generate unit tests    
- Code review    
- Refactoring    
- Technical documentation

However, in Chain of Truth, AI does not generate code based on free prompts. AI must use validated Sources of Truth as the main context. This way, the quality and consistency of implementation output can be better maintained.

### Output of Phase 6

This phase produces:

- Frontend Application    
- Backend Services    
- Database Schema    
- API Implementation    
- Integrated System    

These outputs are not considered complete until they successfully pass the testing phase.

### Key Principle of Phase 6

The focus of this phase is not creating new designs or changing requirements, but implementing previously agreed artifacts.

If during implementation new needs or discrepancies are discovered, changes are not made directly to the code. The team must trace the related source artifacts, fix them, re-validate, and then update the implementation. This principle keeps the code aligned with the Sources of Truth and prevents undocumented changes from appearing.

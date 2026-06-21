After user flows are validated through User Flows, the next stage is to build the **Data Model**. This phase aims to translate business process requirements into the data structure that will be used by the system. The Data Model defines business objects, attributes, entity relationships, validation rules, and data constraints needed to support all agreed use cases.

In Chain of Truth, the Data Model is not derived directly from the SRS, but from **Validated User Flows (SoT #4)**. The reason is simple: user flows show how data is created, read, updated, validated, and used in real business processes. Thus, the resulting data structure is more aligned with the system's operational needs.

### What is Built?

The Data Model can include:

- Domain entities    
- Business objects    
- Attributes and data types    
- Entity relationships    
- Cardinality    
- Validation rules    
- Business constraints    
- Lifecycle or state transitions    
- Persistence requirements    

Simple example:

If in a User Flow there is a process:

```text
User creates an order
↓
System saves the order
↓
User makes a payment
↓
Order changes to Paid
```

Then entities like the following are likely to appear:

- User    
- Order    
- Payment    

Along with their relationships and business rules.

### Why is the Data Model Built After User Flow?

Traditional approaches often start design from the database first. In practice, this often results in data structures that do not truly reflect business processes.

Chain of Truth uses the opposite approach:

```text
User Flow
      ↓
Data Model
```

This means data is shaped based on process needs, not processes being forced to follow the database structure.

This approach helps ensure that every entity and attribute has a clear reason for existence and can be traced back to the use case that requires it.

### Data Model Validation

Before becoming a Source of Truth, the Data Model needs to be reviewed to ensure:

- All User Flows can be supported.    
- No missing entities.    
- Entity relationships are correct.    
- Business rules are accommodated.    
- The data structure is flexible enough for system needs.    

If it is found that a User Flow cannot be implemented with the existing data model, revisions are made to the Data Model before the process continues.

### Output of Phase 4

This phase produces:

|Source of Truth|Description|
|---|---|
|SoT #6|Validated Data Model|

The validated Data Model becomes the basis for:

- Database design    
- Backend implementation    
- API design    
- Validation rules    
- Business logic    
- Integration contracts (UCIC)    

### Key Principle of Phase 4

The focus of this phase is not building a database, but building a **shared understanding of the business data** used by the system.

By making User Flow the main source, the Data Model not only answers _"what data is stored?"_, but also _"why is that data needed and how is it used in business processes?"_. This principle strengthens traceability from requirements to implementation, while ensuring that the data structure always has a clear relationship with user needs.

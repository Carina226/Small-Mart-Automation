# 1. Scope, Subsystems, and Modeling Conventions

The system is decomposed into four cohesive functional subsystems. These cover all eleven use cases from Part 2 without introducing user-interface designs. A system sequence diagram (SSD) treats the complete application as one black-box System lifeline and records externally observable messages, following the purpose of Marsic Figure 2-20. Later design sequence diagrams deliberately expose collaborating software objects, as in Figures 2-32 and 2-33.

| Subsystem | Covered use cases | Primary actors |
|---|---|---|
| Catalog and Inventory | UC01, UC02, UC05, UC06 | Manager, Inventory Clerk |
| Point of Sale and Returns | UC03, UC04 | Cashier, Customer |
| Administration and Oversight | UC07, UC08, UC09 | Manager |
| Loyalty and Offline Reconciliation | UC10, UC11 | Cashier, Customer, Sync Service |

Conventions: 1 means exactly one; 0..* means zero or more. An association describes a meaningful business relationship, not necessarily a database foreign key. Proposed class operations are design decisions and should be validated during implementation.

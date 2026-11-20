# 8. Design Sequence Diagrams and Design Principles

Unlike the black-box SSDs, these diagrams allocate work to collaborating objects. They illustrate proposed controller/service/repository responsibilities, informed by Marsic Section 2.6.1 and the principles of high cohesion, low coupling, information hiding, and separation of concerns discussed in Pressman and Maxim, Chapter 9. Alternative branches are described immediately after each diagram.

## 8.1 Receive Stock

![Figure 8.1 - Receive Stock Design Sequence Diagram](receive-stock-sequence.png)

**Figure 8.1.** Proposed design-level sequence diagram for Receive stock.

**Design rationale:** A cohesive service coordinates the use-case workflow; repositories manage retrieval and persistence; the stock ledger owns quantity-changing records. Failed validation or authorization returns an error without committing. For offline sync, the unique client transaction ID prevents duplicate sale posting and duplicate stock deduction. Diagram messages show the main success path; these failure paths are mandatory implementation conditions.

## 8.2 Process Sale

![Figure 8.2 - Process Sale Design Sequence Diagram](process-sale-sequence.png)

**Figure 8.2.** Proposed design-level sequence diagram for Process sale.

**Design rationale:** A cohesive service coordinates the use-case workflow; repositories manage retrieval and persistence; the stock ledger owns quantity-changing records. Failed validation or authorization returns an error without committing. For offline sync, the unique client transaction ID prevents duplicate sale posting and duplicate stock deduction. Diagram messages show the main success path; these failure paths are mandatory implementation conditions.

## 8.3 Approve Reorder

![Figure 8.3 - Approve Reorder Design Sequence Diagram](approve-reorder-sequence.png)

**Figure 8.3.** Proposed design-level sequence diagram for Approve reorder.

**Design rationale:** A cohesive service coordinates the use-case workflow; repositories manage retrieval and persistence; the stock ledger owns quantity-changing records. Failed validation or authorization returns an error without committing. For offline sync, the unique client transaction ID prevents duplicate sale posting and duplicate stock deduction. Diagram messages show the main success path; these failure paths are mandatory implementation conditions.

## 8.4 Reconcile Offline Sales

![Figure 8.4 - Reconcile Offline Sales Design Sequence Diagram](offline-sync-sequence.png)

**Figure 8.4.** Proposed design-level sequence diagram for Reconcile offline sales.

**Design rationale:** A cohesive service coordinates the use-case workflow; repositories manage retrieval and persistence; the stock ledger owns quantity-changing records. Failed validation or authorization returns an error without committing. For offline sync, the unique client transaction ID prevents duplicate sale posting and duplicate stock deduction. Diagram messages show the main success path; these failure paths are mandatory implementation conditions.

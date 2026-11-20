# 7. Use-Case-to-Domain-Model Traceability

An X indicates that a domain concept is essential to realizing the use case. This is an analysis traceability matrix, modeled after the purpose of Marsic Figure 2-28. Split panels keep the text legible.

## 7.1 Catalog and Inventory Concepts

| Use case | Product | StockBatch | StockMovement | Supplier | PurchaseOrder | InventoryAlert |
|---|---|---|---|---|---|---|
| UC01 | X | | | | | |
| UC02 | X | X | X | | | |
| UC03 | X | | X | | | |
| UC04 | X | | X | | | |
| UC05 | X | X | | | | X |
| UC06 | X | | | X | X | X |
| UC07 | | | | | | |
| UC08 | X | | | | | |
| UC09 | | | | | | |
| UC10 | | | | | | |
| UC11 | | | X | | | |

## 7.2 Point of Sale, Returns, and Employee Concepts

| Use case | Sale | SaleLine | Payment | Receipt | Return | Employee |
|---|---|---|---|---|---|---|
| UC01 | | | | | | X |
| UC02 | | | | | | X |
| UC03 | X | X | X | X | | |
| UC04 | X | | | | X | |
| UC05 | | | | | | |
| UC06 | | | | | | |
| UC07 | | | | | | X |
| UC08 | X | | | | | |
| UC09 | | | | | | X |
| UC10 | X | | | | | |
| UC11 | X | | | | | |

## 7.3 Administration and Loyalty Concepts

| Use case | Role | Shift | AuditEvent | Report | LoyaltyAccount | LoyaltyEntry |
|---|---|---|---|---|---|---|
| UC01 | X | | | | | |
| UC02 | | | | | | |
| UC03 | | | | | | |
| UC04 | | | | | | |
| UC05 | | | | | | |
| UC06 | | | | | | |
| UC07 | X | X | X | | | |
| UC08 | | | | X | | |
| UC09 | | | X | | | |
| UC10 | | | | | X | X |
| UC11 | | | | | | |

## 7.4 Offline Reconciliation Concepts

| Use case | OfflineTransaction | SyncAttempt |
|---|---|---|
| UC01 | | |
| UC02 | | |
| UC03 | | |
| UC04 | | |
| UC05 | | |
| UC06 | | |
| UC07 | | |
| UC08 | | |
| UC09 | | |
| UC10 | | |
| UC11 | X | X | |

## Interpretation

The traceability matrix connects the eleven use cases from the requirements documentation to the domain concepts needed to support them. The X markers show which concepts participate in each use case. These mappings support coverage checks and help ensure that the later design model addresses the requirements.

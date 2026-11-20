# 11. Domain-Model-to-Class-Diagram Traceability

The mapping follows the purpose of Marsic Figure 2-36: distinguish domain concepts that become software classes from domain concepts handled within a service or repository. “Mapped” does not imply that every domain concept requires its own class in the first implementation.

| Domain concept | Design class / owner | Mapping decision |
|---|---|---|
| Product | Product | Direct entity |
| StockBatch | InventoryService / StockLedger | Managed through inventory workflow; standalone entity optional |
| StockMovement | StockLedger | Movement represented in ledger |
| Supplier | PurchaseOrder / repository | Supplier data referenced by reorder process |
| PurchaseOrder | PurchaseOrder | Direct entity |
| InventoryAlert | InventoryService | Derived alert representation |
| Sale | Sale | Direct entity |
| SaleLine | SaleLine | Direct entity |
| Payment | PaymentService | Payment record model may be added |
| Receipt | SalesService | Receipt generated from completed sale |
| Return | ReturnsService | Return record model may be added |
| Employee | Employee | Direct entity |
| Role | Role | Direct entity |
| Shift | EmployeeService | Shift model may be added |
| AuditEvent | AuditService | Audit record persisted by service |
| Report | ReportingService | Generated report value object |
| LoyaltyAccount | LoyaltyAccount | Direct entity |
| LoyaltyEntry | LoyaltyService | Point entry handled by service |
| OfflineTransaction | OfflineTransaction | Direct entity |
| SyncAttempt | SyncCoordinator | Attempt status tracked by coordinator |

# 4. Responsibility Description Tables — Concept Discovery

These tables adapt the responsibility-identification approach of Marsic Tables 2-5 and 2-6. Responsibilities describe what must be known or accomplished.

| Concept | Primary responsibility | Use case |
|---|---|---|
| Product | Maintain SKU, price, category and reorder threshold | UC01 |
| StockBatch | Record received quantities, batch and expiry | UC02 |
| StockMovement | Represent auditable changes in sellable stock | UC02–UC04 |
| InventoryAlert | Represent low-stock and near-expiry conditions | UC05 |
| PurchaseOrder | Record recommendation and manager decision | UC06 |
| Sale | Represent checkout lifecycle and totals | UC03 |
| SaleLine | Capture quantity and price at purchase | UC03 |
| Payment | Record payment authorization result | UC03 |
| Return | Represent eligibility, reason and disposition | UC04 |
| Employee | Maintain staff identity and employment status | UC07 |
| Role | Define authorized business actions | UC07 |
| Report | Summarize sales and inventory for selected dates | UC08 |
| AuditEvent | Capture override, void and discrepancy events | UC09 |
| LoyaltyAccount | Track redeemable point balance | UC10 |
| OfflineTransaction | Retain unique queued sale until reconciliation | UC11 |

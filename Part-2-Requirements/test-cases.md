
# Small Mart Automation - Acceptance Test Cases

**Course:** COSC-3506-F01X  
**Project:** Small Mart Automation  
**Part:** 2 - Requirements Documentation  
**Prepared by:** Karina Thapa  

## 8. Acceptance Test Cases

Each test includes an identifier, mapped use case, pass/fail criterion, input data, procedure and expected result.

These are planned acceptance tests; no execution results are claimed.

---

### TC01 - UC01: Manage Products

| Field | Value |
|---|---|
| Use case tested | UC01 |
| Pass/fail criterion | Product stored; appears in product list |
| Input data | Manager enters SKU A100, price 3.49 |
| Test procedure | Save product |
| Expected result | Product stored; appears in product list |
| Execution status | Not run - planned acceptance test |

### TC02 - UC02: Receive Stock

| Field | Value |
|---|---|
| Use case tested | UC02 |
| Pass/fail criterion | Quantity increases by 20 and receipt is logged |
| Input data | SKU A100, +20 units, future expiry |
| Test procedure | Receive shipment |
| Expected result | Quantity increases by 20 and receipt is logged |
| Execution status | Not run - planned acceptance test |

### TC03 - UC03: Process Sale

| Field | Value |
|---|---|
| Use case tested | UC03 |
| Pass/fail criterion | One sale recorded; quantity decreases by 2; receipt issued |
| Input data | SKU A100, qty 2, approved payment |
| Test procedure | Scan and pay |
| Expected result | One sale recorded; quantity decreases by 2; receipt issued |
| Execution status | Not run - planned acceptance test |

### TC04 - UC03: Process Sale (Out of Stock)

| Field | Value |
|---|---|
| Use case tested | UC03 |
| Pass/fail criterion | Sale blocked; quantity unchanged |
| Input data | SKU with quantity 0 |
| Test procedure | Attempt checkout |
| Expected result | Sale blocked; quantity unchanged |
| Execution status | Not run - planned acceptance test |

### TC05 - UC04: Process Return

| Field | Value |
|---|---|
| Use case tested | UC04 |
| Pass/fail criterion | Return recorded; eligible stock increases by 1 |
| Input data | Prior sale of 2 units; return 1 |
| Test procedure | Process return |
| Expected result | Return recorded; eligible stock increases by 1 |
| Execution status | Not run - planned acceptance test |

### TC06 - UC05: Monitor Inventory Alerts

| Field | Value |
|---|---|
| Use case tested | UC05 |
| Pass/fail criterion | SKU flagged as low stock |
| Input data | SKU quantity 4, threshold 5 |
| Test procedure | Open alerts |
| Expected result | SKU flagged as low stock |
| Execution status | Not run - planned acceptance test |

### TC07 - UC06: Approve Reorder

| Field | Value |
|---|---|
| Use case tested | UC06 |
| Pass/fail criterion | Purchase order saved as approved |
| Input data | Valid supplier and proposed qty 15 |
| Test procedure | Approve order |
| Expected result | Purchase order saved as approved |
| Execution status | Not run - planned acceptance test |

### TC08 - UC07: Manage Employees

| Field | Value |
|---|---|
| Use case tested | UC07 |
| Pass/fail criterion | Access denied and event audited |
| Input data | Cashier attempts role edit |
| Test procedure | Open employee permissions |
| Expected result | Access denied and event audited |
| Execution status | Not run - planned acceptance test |

### TC09 - UC08: View Reports

| Field | Value |
|---|---|
| Use case tested | UC08 |
| Pass/fail criterion | Report totals match recorded sales |
| Input data | Two completed sales in range |
| Test procedure | Run daily report |
| Expected result | Report totals match recorded sales |
| Execution status | Not run - planned acceptance test |

### TC10 - UC09: Review Exception Logs

| Field | Value |
|---|---|
| Use case tested | UC09 |
| Pass/fail criterion | Override appears with timestamp/actor |
| Input data | Recorded manual price override |
| Test procedure | Open exception log |
| Expected result | Override appears with timestamp/actor |
| Execution status | Not run - planned acceptance test |

### TC11 - UC10: Manage Loyalty

| Field | Value |
|---|---|
| Use case tested | UC10 |
| Pass/fail criterion | 10 points applied; balance adjusted once |
| Input data | Account with 20 points, redeem 10 |
| Test procedure | Redeem at checkout |
| Expected result | 10 points applied; balance adjusted once |
| Execution status | Not run - planned acceptance test |

### TC12 - UC11: Sync Offline Transactions

| Field | Value |
|---|---|
| Use case tested | UC11 |
| Pass/fail criterion | Exactly one sale persisted and one inventory deduction |
| Input data | One queued sale, reconnection and repeated submission |
| Test procedure | Reconnect and sync twice |
| Expected result | Exactly one sale persisted and one inventory deduction |
| Execution status | Not run - planned acceptance test |

### TC13 - UC03: Process Sale (Rejected Payment)

| Field | Value |
|---|---|
| Use case tested | UC03 |
| Pass/fail criterion | No completed sale and no stock deduction |
| Input data | SKU A100 qty 1; payment rejected |
| Test procedure | Attempt payment |
| Expected result | No completed sale and no stock deduction |
| Execution status | Not run - planned acceptance test |

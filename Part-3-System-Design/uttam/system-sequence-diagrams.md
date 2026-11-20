# 2. System Sequence Diagrams and Explanations

System sequence diagrams treat the complete application as one black-box System lifeline and record externally observable messages, following Marsic Figure 2-20.

## 2.1 Catalog and Inventory

![Figure 2.1 Catalog and Inventory](catalog-inventory-ssd.png)

**Figure 2.1:** Black-box system sequence diagram for Catalog and Inventory; adapted in method from Marsic Figure 2-20.

| Step | Sender | Receiver | Message |
|---|---|---|---|
| 1 | Manager | System | create/update product(SKU, price, threshold) |
| 2 | System | Manager | validation and save status |
| 3 | Inventory Clerk | System | receive shipment(SKU, quantity, batch, expiry) |
| 4 | System | Inventory Clerk | receipt and updated stock |
| 5 | Inventory Clerk | System | request low-stock/expiry alerts |
| 6 | System | Inventory Clerk | alert list |
| 7 | Manager | System | approve reorder(orderId) |
| 8 | System | Manager | purchase-order status |

**Coverage:** UC01, UC02, UC05, UC06.

The subsystem receives business requests from manager and inventory clerk and returns confirmations, data, or validation failures. All internal validation and persistence are intentionally hidden behind the System boundary. Alternative paths include unauthorized access, invalid data, and unavailable services. For inventory and sales, failed operations must not leave partial stock updates (NFR04).

## 2.2 Point of Sale and Returns

![Figure 2.2 Point of Sale and Returns](point-of-sale-ssd.png)

**Figure 2.2:** Black-box system sequence diagram for Point of Sale and Returns; adapted in method from Marsic Figure 2-20.

| Step | Sender | Receiver | Message |
|---|---|---|---|
| 1 | Cashier | System | start sale and scan SKU |
| 2 | System | Cashier | item price and availability |
| 3 | Cashier | System | confirm payment and checkout |
| 4 | System | Cashier | sale status and receipt |
| 5 | Cashier | System | request return(receipt, items, reason) |
| 6 | System | Cashier | return eligibility |
| 7 | Cashier | System | confirm authorized return |
| 8 | System | Cashier | refund and stock disposition |

**Coverage:** UC03, UC04.

The subsystem receives business requests from cashier and customer and returns confirmations, data, or validation failures. All internal validation and persistence are intentionally hidden behind the System boundary. Alternative paths include unauthorized access, invalid data, and unavailable services. For inventory and sales, failed operations must not leave partial stock updates (NFR04).

## 2.3 Administration and Oversight

![Figure 2.3 Administration and Oversight](administration-ssd.png)

**Figure 2.3:** Black-box system sequence diagram for Administration and Oversight; adapted in method from Marsic Figure 2-20.

| Step | Sender | Receiver | Message |
|---|---|---|---|
| 1 | Manager | System | manage employee role or schedule |
| 2 | System | Manager | save and audit result |
| 3 | Manager | System | request sales/stock report(date range) |
| 4 | System | Manager | report totals |
| 5 | Manager | System | request exception log(filters) |
| 6 | System | Manager | voids, overrides, discrepancies |
| 7 | Manager | System | record review outcome |
| 8 | System | Manager | review confirmation |

**Coverage:** UC07, UC08, UC09.

The subsystem receives business requests from manager and returns confirmations, data, or validation failures. All internal validation and persistence are intentionally hidden behind the System boundary. Alternative paths include unauthorized access, invalid data, and unavailable services. For inventory and sales, failed operations must not leave partial stock updates (NFR04).

## 2.4 Loyalty and Offline Reconciliation

![Figure 2.4 Loyalty and Offline Reconciliation](loyalty-offline-ssd.png)

**Figure 2.4:** Black-box system sequence diagram for Loyalty and Offline Reconciliation; adapted in method from Marsic Figure 2-20.

| Step | Sender | Receiver | Message |
|---|---|---|---|
| 1 | Cashier | System | lookup loyalty account |
| 2 | System | Cashier | points balance |
| 3 | Cashier | System | redeem eligible points |
| 4 | System | Cashier | redemption outcome |
| 5 | Cashier | System | queue permitted offline sale |
| 6 | Sync Service | System | submit queued transactions after reconnection |
| 7 | System | Sync Service | deduplication/conflict status |
| 8 | System | Cashier | final reconciliation status |

**Coverage:** UC10, UC11.

The subsystem receives business requests from cashier, customer and sync service and returns confirmations, data, or validation failures. All internal validation and persistence are intentionally hidden behind the System boundary. Alternative paths include unauthorized access, invalid data, and unavailable services. For inventory and sales, failed operations must not leave partial stock updates (NFR04).

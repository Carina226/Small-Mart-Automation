
# Small Mart Automation - Detailed Use-Case Descriptions

**Course:** COSC-3506-F01X  
**Project:** Small Mart Automation  
**Part:** 2 - Requirements Documentation  
**Prepared by:** Malik Wasif  

## 7. Detailed Use-Case Descriptions

### UC01: Manage products

**Related requirements:** REQ01, REQ02, NFR01

**Initiating actor:** Manager

**Actor goal:** Manage products

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Manager selects product management.
2. System displays product list.
3. Manager enters or edits SKU, price, category and threshold.
4. System validates and saves product record.

**Extensions / alternative scenarios:**
- 1a. Duplicate SKU or invalid price: reject and explain; unauthorized user: deny and log.

---

### UC02: Receive stock

**Related requirements:** REQ01, REQ03, REQ04, NFR01

**Initiating actor:** Inventory Clerk

**Actor goal:** Receive stock

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Clerk selects receive shipment.
2. System requests supplier, SKU, quantity, batch and expiry.
3. Clerk confirms delivered items.
4. System records receipt and increases stock.

**Extensions / alternative scenarios:**
- 1a. Unknown SKU: require product lookup/correction; invalid quantity: reject; expiry in past: flag for review.

---

### UC03: Process sale

**Related requirements:** REQ01, REQ05, REQ06, REQ08, NFR02, NFR04

**Initiating actor:** Cashier

**Actor goal:** Process sale

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Cashier starts sale and scans SKU.
2. System retrieves price and verifies quantity.
3. Cashier confirms items, discounts and payment.
4. System records sale, deducts stock and issues receipt.

**Extensions / alternative scenarios:**
- 1a. Insufficient stock: prevent checkout of affected item; payment failure: do not commit sale; network loss: follow UC11.

---

### UC04: Process return

**Related requirements:** REQ01, REQ04, REQ07, NFR04

**Initiating actor:** Cashier

**Actor goal:** Process return

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Cashier locates original sale.
2. System displays eligible return items.
3. Cashier selects quantity and reason.
4. System records return and adjusts eligible inventory.

**Extensions / alternative scenarios:**
- 1a. Unknown receipt or excessive return quantity: reject; damaged item: do not return to sellable stock.

---

### UC05: Monitor inventory alerts

**Related requirements:** REQ04, REQ09

**Initiating actor:** Inventory Clerk / Manager

**Actor goal:** Monitor inventory alerts

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Clerk or manager opens inventory alerts.
2. System compares stock to thresholds and checks expiry dates.
3. System displays flagged items and relevant quantities.
4. Actor reviews or acknowledges alerts.

**Extensions / alternative scenarios:**
- 1a. No alerts: show empty state; missing expiry: mark unknown rather than invent date.

---

### UC06: Approve reorder

**Related requirements:** REQ09, REQ10

**Initiating actor:** Manager

**Actor goal:** Approve reorder

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Manager opens reorder recommendations.
2. System displays SKU, supplier and proposed quantities.
3. Manager approves, edits or rejects recommendation.
4. System saves purchase order status.

**Extensions / alternative scenarios:**
- 1a. Missing supplier: request supplier assignment; invalid quantity: reject.

---

### UC07: Manage employees

**Related requirements:** REQ01, REQ11, NFR01

**Initiating actor:** Manager

**Actor goal:** Manage employees

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Manager opens employee management.
2. System lists staff profiles and roles.
3. Manager changes profile, schedule or permission.
4. System saves and audits the change.

**Extensions / alternative scenarios:**
- 1a. Unauthorized access: deny; conflicting shift or invalid fields: request correction.

---

### UC08: View reports

**Related requirements:** REQ12

**Initiating actor:** Manager

**Actor goal:** View reports

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Manager selects date range and report.
2. System aggregates sales and inventory data.
3. System displays revenue, products and stock metrics.

**Extensions / alternative scenarios:**
- 1a. No data: display zero/empty report; invalid range: prompt correction.

---

### UC09: Review exception logs

**Related requirements:** REQ13, NFR01

**Initiating actor:** Manager

**Actor goal:** Review exception logs

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Manager opens exception log.
2. System shows voids, overrides and discrepancies.
3. Manager filters and reviews events.
4. System records review outcome if provided.

**Extensions / alternative scenarios:**
- 1a. No events: show empty log; insufficient permission: deny.

---

### UC10: Manage loyalty

**Related requirements:** REQ14

**Initiating actor:** Customer / Cashier

**Actor goal:** Manage loyalty

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Customer provides loyalty identifier through cashier.
2. System retrieves available points.
3. Cashier applies eligible redemption or awards points after sale.
4. System updates loyalty balance.

**Extensions / alternative scenarios:**
- 1a. Account not found: continue normal sale; insufficient points: reject redemption.

---

### UC11: Sync offline transactions

**Related requirements:** REQ06, NFR03, NFR04

**Initiating actor:** Cashier / System

**Actor goal:** Sync offline transactions

**Participating actors:** Application/database service; supporting staff as appropriate

**Preconditions:** Actor has appropriate access; required product or transaction data exists where applicable.

**Postconditions:** Successful operation is recorded with consistent inventory and audit state; on failure, no partial update.

**Main success scenario:**
1. Cashier continues permitted POS operations during outage.
2. System queues uniquely identified transactions locally.
3. Connection returns and sync service submits queued transactions.
4. System reconciles duplicates/conflicts and confirms final stock.

**Extensions / alternative scenarios:**
- 1a. Sync failure: retain queue and show status; duplicate transaction: do not double-deduct stock.

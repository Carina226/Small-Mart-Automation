# 12. Design Validation and Requirements Coverage

| Design concern | Requirements | Validation criterion |
|---|---|---|
| Role-based authorization | REQ01, NFR01 | Reject unauthorized actions and audit privileged changes |
| Inventory consistency | REQ04, REQ06, NFR04 | No partial deduction when sale/payment fails |
| Receipt generation | REQ08 | Exactly one receipt for each completed sale |
| Low stock and expiry | REQ09 | Alert threshold and expiry checks use recorded data |
| Offline idempotency | NFR03, NFR04 | Repeated sync does not duplicate sale or stock deduction |
| Loyalty extension | REQ14 | Points updated only for eligible completed transactions |

## Coverage Review

UC01–UC11 are included in the subsystem SSDs and domain traceability. Design sequence diagrams focus on four representative high-impact interactions, with class-level responsibilities and tables covering the remaining use cases.

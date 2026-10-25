
# Small Mart Automation - Requirements Traceability Matrix

**Course:** COSC-3506-F01X  
**Project:** Small Mart Automation  
**Part:** 2 - Requirements Documentation  
**Prepared by:** Mausam Bista  

## 5. Requirements-to-Use-Case Traceability and Sizing

An X indicates that a use case addresses the requirement. The maximum priority weight and total priority weight of linked requirements are reported per use case, following the intent of Marsic Figure 2-18. Each use case also has an independent relative size.

**Priority Weight (PW):** 1 to 5, where 5 is the highest priority.

**Use-Case Size:** S = Small, M = Medium, L = Large.

### Table 1: Requirements Traceability Matrix (UC01-UC06)

| Requirement | PW | UC01 | UC02 | UC03 | UC04 | UC05 | UC06 |
|---|---|---|---|---|---|---|---|
| REQ01 | 5 | X | X | X | X | | |
| REQ02 | 5 | X | | | | | |
| REQ03 | 5 | | X | | | | |
| REQ04 | 5 | | X | | X | X | |
| REQ05 | 5 | | | X | | | |
| REQ06 | 5 | | | X | | | |
| REQ07 | 4 | | | | X | | |
| REQ08 | 5 | | | X | | | |
| REQ09 | 4 | | | | | X | X |
| REQ10 | 4 | | | | | | X |
| REQ11 | 3 | | | | | | |
| REQ12 | 4 | | | | | | |
| REQ13 | 3 | | | | | | |
| REQ14 | 2 | | | | | | |
| NFR01 | 5 | X | X | | | | |
| NFR02 | 5 | | | X | | | |
| NFR03 | 4 | | | | | | |
| NFR04 | 5 | | | X | X | | |
| **Max PW** | | **5** | **5** | **5** | **5** | **5** | **4** |
| **Total PW** | | **15** | **20** | **30** | **19** | **9** | **8** |
| **UC size** | | **M** | **L** | **L** | **M** | **M** | **M** |

### Table 2: Requirements Traceability Matrix (UC07-UC11)

| Requirement | PW | UC07 | UC08 | UC09 | UC10 | UC11 |
|---|---|---|---|---|---|---|
| REQ01 | 5 | X | | | | |
| REQ02 | 5 | | | | | |
| REQ03 | 5 | | | | | |
| REQ04 | 5 | | | | | |
| REQ05 | 5 | | | | | |
| REQ06 | 5 | | | | | X |
| REQ07 | 4 | | | | | |
| REQ08 | 5 | | | | | |
| REQ09 | 4 | | | | | |
| REQ10 | 4 | | | | | |
| REQ11 | 3 | X | | | | |
| REQ12 | 4 | | X | | | |
| REQ13 | 3 | | | X | | |
| REQ14 | 2 | | | | X | |
| NFR01 | 5 | X | | X | | |
| NFR02 | 5 | | | | | |
| NFR03 | 4 | | | | | X |
| NFR04 | 5 | | | | | X |
| **Max PW** | | **5** | **4** | **5** | **2** | **5** |
| **Total PW** | | **13** | **4** | **8** | **2** | **14** |
| **UC size** | | **M** | **M** | **M** | **M** | **L** |

### Use-Case Reference

| Use Case ID | Use Case Name | Size |
|---|---|---|
| UC01 | Manage products | M |
| UC02 | Receive stock | L |
| UC03 | Process sale | L |
| UC04 | Process return | M |
| UC05 | Monitor inventory alerts | M |
| UC06 | Approve reorder | M |
| UC07 | Manage employees | M |
| UC08 | View reports | M |
| UC09 | Review exception logs | M |
| UC10 | Manage loyalty | M |
| UC11 | Sync offline transactions | L |

### Explanation

- **X:** Indicates that a use case addresses the corresponding requirement.
- **PW:** Priority weight assigned to a requirement.
- **Max PW:** Highest priority weight among the requirements linked to a use case.
- **Total PW:** Sum of the priority weights of all requirements linked to a use case.
- **UC size:** Independent relative size estimate for a use case.

The traceability matrix helps identify which use cases address each functional and non-functional requirement and supports prioritization and effort planning.

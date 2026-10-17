# DFD Consistency Check

This file confirms that the Lab 4 data flow models are consistent with each other and with the Lab 3 requirements.

## 1. External entities vs. Use Case actors

| Lab 3 Use Case actor | Context Diagram | Level-0 DFD |
|---|---|---|
| Employee | Yes | Yes (1.0–7.0) |
| Manager | Yes | Yes (3.0, 5.0) |
| HR Department | Yes | Yes (1.0, 7.0) |
| Finance Department | Yes | Yes (4.0) |
| System Administrator | Yes | Yes (1.0) |

No entity appears in the DFDs that is not an actor in the [Use Case Diagram](../Requirements/Use_Case_Diagram).

## 2. Balancing: Context Diagram vs. Level-0 DFD

| External entity | Context Diagram flow | Direction | Level-0 process |
|---|---|---|---|
| Employee | Credentials, requests, profile changes, policy questions and viewing queries | In | 1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0 |
| Employee | Access results and employee information; request status, documents and answers; announcements and notifications | Out | 1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0 |
| Manager | Leave queries and approval decisions; asset-extension decisions | In | 3.0, 5.0 |
| Manager | Pending leave and extension requests; confirmations | Out | 3.0, 5.0 |
| HR Department | Announcement data and profile verification decisions | In | 7.0, 1.0 |
| HR Department | Pending profile changes and publication confirmations | Out | 1.0, 7.0 |
| Finance Department | Finance outcomes and payslip records | In | 4.0 |
| Finance Department | Expense claims, discrepancy reports and payslip queries | Out | 4.0 |
| System Administrator | Role and permission changes | In | 1.0 |
| System Administrator | Update confirmations | Out | 1.0 |

Every flow on the Context Diagram enters or leaves a Level-0 process, and no new external flow appears at Level 0, so the two diagrams are balanced.

## 3. Checklist

| Check | Status | Evidence |
|---|---|---|
| Context Diagram shows ONE as a single process (0.0) | Yes | No internal processes or data stores on the Context Diagram |
| External entities match the Use Case actors | Yes | Section 1 |
| Level-0 DFD uses the same external entities | Yes | Section 1 |
| Context Diagram and Level-0 DFD are balanced | Yes | Section 2 |
| Level-0 has at least 5 meaningful processes | Yes | 7 processes (1.0–7.0) |
| Level-0 has at least 2 data stores | Yes | D1 Employee records, D2 Service requests, D3 Company content |
| Core Processes Matrix matches the Level-0 processes | Yes | [Core_Processes_Matrix.md](Core_Processes_Matrix.md) lists the same 1.0–7.0 with the same entities and stores |
| Processes match the Functional Requirements and Use Cases | Yes | See the [Functional Requirements](../Requirements/Functional_Requirements.md) and [Use Cases](../Requirements/Use_Cases.md) |
| Data stores match the WBS database design | Yes | WBS task T2 designs the three logical stores D1–D3 |

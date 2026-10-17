# Work Breakdown Structure (WBS)

The WBS lists the actual work needed to build the ONE ERP App. The prototype is delivered in five increments.

| ID | Task Name | Description | Predecessor(s) | Duration (Days) |
|---|---|---|---|---|
| T1 | Confirm ONE requirements and interfaces | Confirm the Lab 3 baseline and define prototype data contracts. | — | 3 |
| T2 | Design database and audit records | Design tables within the three logical stores for employee records, service requests and company content. | T1 | 4 |
| T3 | Design employee and approval interfaces | Design the dashboard, employee forms and Manager, HR and Finance views. | T1 | 3 |
| T4 | Build login, profile, directory and dashboard shell | Deliver increment 1 with role checks, profile access, directory search and the dashboard structure. | T2, T3 | 5 |
| T5 | Build internal attendance and payslip adapter | Provide authorized mock attendance and payslip data, timeouts and cached-data handling. | T2 | 4 |
| T6 | Build attendance dashboard and leave workflows | Deliver increment 2 with attendance summaries, leave validation and manager decisions. | T4, T5 | 6 |
| T7 | Test increment 2 and shared request handling | Test permissions, leave and attendance; stabilize common request records before further modules. | T6 | 2 |
| T8 | Build expenses and payslip enquiries | Deliver increment 3 with receipt uploads, Finance outcomes, payslip access and discrepancies. | T7 | 5 |
| T9 | Build IT assets and support | Deliver increment 4 with borrowing, extensions, returns, ticket submission and tracking. | T7 | 5 |
| T10 | Prepare approved documents and ONEAI retrieval | Build authorized document retrieval and source-grounded policy answers. | T4 | 4 |
| T11 | Integrate announcements, notifications and ONEAI | Deliver increment 5 and connect all modules to the employee dashboard. | T8, T9, T10 | 4 |
| T12 | Run end-to-end and quality acceptance tests | Run regression, access-control, upload, backup/recovery and performance checks. | T11 | 4 |
| T13 | Prepare demonstration, deployment and documentation | Package the prototype, user guide, technical report and final demonstration. | T12 | 2 |

**Total work:** 51 task-days. **Project duration:** 35 days, because several tasks run in parallel. See the [Critical Path](Critical_Path.md).

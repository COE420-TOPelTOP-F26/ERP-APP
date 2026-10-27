# Class model consistency check

| Use cases/workflow | Requirements | Model support | DFD/store |
|---|---|---|---|
| UC-01, UC-02 | FR-01–FR-03 | LeaveRequest, LeaveBalance, Manager, ApprovalDecision and notifications. | 3.0 / D2 |
| UC-03 | FR-04 | ExpenseClaim, ExpenseItem, Attachment; Finance reviews the claim. | 4.0 / D2 |
| UC-04 | Lab 2 assets scope; S-05 | AssetRequest (BORROW), ITAsset, AssetLoan; IT confirms handover. | 5.0 / D2 |
| UC-05 | FR-05 | ONEAIAssistant, AIQuery, AIResponse and approved accessible Document sources. | 6.0 / D3 |
| UC-06 | FR-06 | AttendanceAdapter imports AttendanceRecord; AttendanceSummary totals weekly hours. | 2.0 / D1 |
| UC-07 | FR-07 | EmployeeDirectory searches Employee by name, department or position. | 1.0 / D1 |
| UC-08, UC-18 | FR-08, FR-18; S-06 | HROfficer publishes Announcement; employees view it and receive notifications. | 7.0 / D3, D2 |
| UC-09 | Lab 2 payroll scope; NFR-07 | PayrollAdapter retrieves external ERP Payslip and line items; bounded cache fallback. | 4.0 / D1 |
| UC-10 | FR-10 | Request and AuditEntry provide history and current status for every request type. | 3.0 / D2 |
| UC-11 | FR-11 | Dashboard shows attendance, pending requests, upcoming leave, announcements and notices. | 2.0 / D1–D3 |
| UC-12, UC-17 | FR-12, FR-17 | ITSupportTicket and TicketUpdate separate submission from status/latest-update viewing. | 5.0 / D2 |
| UC-13, UC-15 | FR-15; administrator scope | UserAccount, Session, Role, Permission and SystemAdministrator enforce access and role changes. | 1.0 / D1 |
| UC-14 | FR-19 | PayslipDiscrepancyReport references the employee’s Payslip; Finance investigates. | 4.0 / D1, D2 |
| UC-16 | FR-16 | AssetRequest (RETURN), AssetLoan and ITStaff.confirmReturn precede asset-status changes. | 5.0 / D2 |
| UC-19 | FR-13 | DocumentCenter searches; Document checks permission before viewing/downloading. | 6.0 / D3 |
| UC-20 | FR-20 | Employee profile fields, Department and EmergencyContact provide authorized profile data. | 1.0 / D1 |
| Profile changes | FR-14; S-02 | ProfileChangeRequest retains proposed values; HROfficer verifies before apply(). | 1.0 / D1, D2 |
| Asset extensions | FR-09; S-05 | AssetRequest (EXTENSION) routes to the direct manager; IT applies the approved date. | 5.0 / D2 |

| Relationships | Verification |
|---|---|
| Employee access | One UserAccount per Employee; each account has 1..* Roles, and each Role grants 1..* Permissions. Staff inherit Employee self-service behavior. |
| Requests and audit | Each Request has one submitter and 1..* AuditEntries. ApprovalDecision has one accountable reviewer; a request may have 0..* decisions when reviewed again. |
| Assets | Each loan belongs to one employee and asset; at most one loan per asset is open. Extensions/returns require an existing employee-owned loan; return closes it only after IT confirmation. |
| Finance and files | Each ExpenseItem has one receipt Attachment. Each discrepancy concerns the submitter’s Payslip; a payslip owns 1..* line items. |
| Answers and notifications | AIQuery owns 0..1 AIResponse. An answer must cite approved accessible sources; a no-answer response may cite none. Each notification has one recipient and a valid request, announcement or reminder target. |


Consistency findings: add IT as an actor/entity for asset and ticket operations; align UC-06 with weekly attendance; replace outdated D4–D7 references with D1–D3; add a profile-update use case for FR-14 and an explicit borrowing requirement for UC-04. ERP and Attendance are external supporting systems; their adapters belong to ONE. ONEAI answers policy questions only and creates a support ticket after employee confirmation. FR-08/FR-18 announcements need a separate scenario, S-06, rather than policy scenario S-04.

The submitted use-case arrow directions are correct; restore their missing labels: UC-11 «include» UC-06; UC-14 «extend» UC-09; UC-17 «extend» UC-10; UC-19 «extend» UC-05; UC-12 «extend» UC-05. Remove HR → System Administrator; HR does not inherit administrator privileges.
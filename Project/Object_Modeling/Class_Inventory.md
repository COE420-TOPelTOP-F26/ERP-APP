# Approved class inventory

| ID | Class | Responsibility | Use cases | Source IDs |
|---|---|---|---|---|
| C01 | Employee | Employee identity, profile and self-service access. | UC-01, 03–07, 09–12, 14–20 | TA-01, NA-01, RE-02, KE-01, KE-03 |
| C02 | Manager | Direct-report leave and extension decisions. | UC-02 | TA-02 |
| C03 | HROfficer | Profile verification and company-content publication. | UC-08 | NA-02 |
| C04 | FinanceOfficer | Expense and payslip discrepancy review. | UC-03, UC-14 | RE-04 |
| C05 | ITStaff | Asset processing and support-ticket updates. | UC-04, UC-12, UC-16, UC-17 | KE-02 |
| C06 | SystemAdministrator | Accounts, roles and permissions administration. | UC-13 | RE-03 |
| C07 | Department | Department membership and announcement targeting. | UC-07, UC-08, UC-18 | NA-03 |
| C08 | EmergencyContact | Employee emergency contact information. | UC-20 | KE-04 |
| C09 | UserAccount | Credentials, authentication and permission checks. | UC-13, UC-15 | RE-01, RE-08 |
| C10 | Role | Named, assignable set of permissions. | UC-13, UC-15, UC-19 | RE-05 |
| C11 | Permission | One system access right. | UC-13, UC-15 | RE-06 |
| C12 | Session | Activity tracking and 15-minute inactivity expiry. | UC-15 | RE-07 |
| C13 | EmployeeDirectory | Searchable employee directory. | UC-07 | NA-04 |
| C14 | AttendanceRecord | Imported entry/exit record and working hours. | UC-06, UC-11 | NA-05 |
| C15 | AttendanceSummary | Attendance totals for a selected period. | UC-06, UC-11 | NA-06 |
| C16 | Dashboard | Personalized attendance, requests, notices and leave. | UC-11 | RE-09 |
| C17 | Request {abstract} | Shared request identity, lifecycle and validation. | UC-10 | TA-03, NA-12, KE-05 |
| C18 | LeaveRequest | Leave type, dates, reason and validation. | UC-01, UC-02 | TA-04 |
| C19 | LeaveBalance | Leave entitlement, usage and remaining days. | UC-01, UC-02 | TA-05 |
| C20 | ApprovalDecision | Reviewer decision, comment, author and time. | UC-02, UC-03, UC-14 | TA-06 |
| C21 | Attachment | Validated and protected uploaded file. | UC-03, UC-12 | TA-09 |
| C22 | AuditEntry | Attributable request action and timestamp. | UC-10 | NA-14 |
| C23 | ProfileChangeRequest | Proposed profile value pending HR verification. | FR-14; UC missing | New |
| C24 | ExpenseClaim | Travel claim and its expense items. | UC-03 | TA-07 |
| C25 | ExpenseItem | Expense category, amount, date and receipt. | UC-03 | TA-08 |
| C26 | Payslip | ERP payslip and cache retrieval time. | UC-09, UC-14 | NA-09, RE-11 |
| C27 | PayslipLineItem | One payslip earning or deduction. | UC-09, UC-14 | NA-10 |
| C28 | PayslipDiscrepancyReport | Employee’s reported payslip discrepancy. | UC-14 | RE-12 |
| C29 | ITAsset | Equipment identity, details and availability. | UC-04, UC-16 | TA-10, KE-08 |
| C30 | AssetLoan | One borrowing, due date and return. | UC-04, UC-16 | KE-07 |
| C31 | AssetRequest | Borrow, extension or return request. | UC-04, UC-16 (FR-09) | TA-11, NA-13, KE-06 |
| C32 | ITSupportTicket | IT issue, ticket number and progress. | UC-12, UC-17 | RE-10, KE-09 |
| C33 | TicketUpdate | IT-authored ticket message and status. | UC-17 | KE-10 |
| C34 | Document | Authorized policy, form or procedure. | UC-05, UC-19 | TA-15, RE-14, KE-13 |
| C35 | DocumentCenter | Authorized document search and retrieval. | UC-19 | RE-13, KE-12 |
| C36 | ONEAIAssistant | Sourced policy answers and confirmed escalation. | UC-05 | TA-12 |
| C37 | AIQuery | Employee policy question. | UC-05 | TA-13 |
| C38 | AIResponse | Answer, confidence, sources or no-answer flag. | UC-05 | TA-14 |
| C39 | Announcement | HR-published announcement and intended audience. | UC-08, UC-18 | NA-07, KE-11 |
| C40 | Notification | Employee notice linking to its triggering event. | UC-02, UC-08, UC-11 | NA-08 |
| C41 | NotificationService | Notification creation and announcement broadcast. | UC-02, UC-08 | New |
| C42 | IntegrationAdapter {abstract} | Shared API timeout and failure handling. | UC-06, UC-09 | New |
| C43 | AttendanceAdapter | Retrieves records from external attendance source. | UC-06 | New |
| C44 | PayrollAdapter | Retrieves ERP payslips; limits cache to 24 hours. | UC-09 | NA-11 |

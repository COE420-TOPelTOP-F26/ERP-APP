# Individual inventories

Tala Abed g00099746 UC-01–UC-05 (TA)
Nadine Alameldin g00098602 UC-06–UC-10 (NA)
Razan El Gendy g00099305 UC-11–UC-15 (RE)
Kholoud Elkholy g00099492 UC-16–UC-20 (KE)

| ID | Class | Responsibility | Use cases |
|---|---|---|---|
| TA-01 | Employee | Submits employee requests and asks policy questions. | UC-01, UC-03, UC-04, UC-05 |
| TA-02 | Manager | Reviews direct reports’ leave and records decisions. | UC-02 |
| TA-03 | EmployeeRequest {abstract} | Shares request identity, status, submission and validation. | UC-01, UC-03, UC-04 |
| TA-04 | LeaveRequest | Stores leave dates, type and reason. | UC-01, UC-02 |
| TA-05 | LeaveBalance | Checks remaining leave days by type. | UC-01, UC-02 |
| TA-06 | ApprovalDecision | Records a reviewer’s decision, comment and time. | UC-02 |
| TA-07 | TravelExpenseClaim | Groups travel expenses and calculates the claim total. | UC-03 |
| TA-08 | ExpenseItem | Stores an expense category, amount and date. | UC-03 |
| TA-09 | Receipt | Stores the receipt supporting an expense item. | UC-03 |
| TA-10 | ITAsset | Tracks borrowable equipment and availability. | UC-04 |
| TA-11 | AssetBorrowRequest | Requests an asset for a specified period. | UC-04 |
| TA-12 | ONEAIAssistant | Answers policy questions using approved documents. | UC-05 |
| TA-13 | PolicyQuestion | Stores an employee’s policy question. | UC-05 |
| TA-14 | AIAnswer | Stores an answer, confidence and source link. | UC-05 |
| TA-15 | PolicyDocument | Provides an approved source for policy answers. | UC-05 |
| NA-01 | Employee | Owns attendance, payslips and request history. | UC-06, UC-07, UC-09, UC-10 |
| NA-02 | HRUser | Publishes announcements as an authorized HR employee. | UC-08 |
| NA-03 | Department | Groups employees for directory searches. | UC-07 |
| NA-04 | EmployeeDirectory | Searches by name, department or position. | UC-07 |
| NA-05 | AttendanceRecord | Stores daily entry/exit times and working hours. | UC-06 |
| NA-06 | AttendanceSummary | Summarizes weekly attendance records and totals. | UC-06 |
| NA-07 | Announcement | Stores announcement text and publication time. | UC-08 |
| NA-08 | Notification | Shows an employee a triggered notification. | UC-08 |
| NA-09 | Payslip | Represents an ERP salary statement. | UC-09 |
| NA-10 | PayslipItem | Stores an earning or deduction line. | UC-09 |
| NA-11 | ERPConnector | Retrieves ERP payslips and handles cached fallback. | UC-09 |
| NA-12 | ServiceRequest {abstract} | Shares identity and status across request history. | UC-10 |
| NA-13 | AssetExtensionRequest | Requests a later due date for a loan. | UC-10 |
| NA-14 | RequestStatusChange | Records a request’s status change and author. | UC-10 |
| RE-01 | SystemUser {abstract} | Defines common sign-in data and behavior. | UC-13, UC-15 |
| RE-02 | EmployeeUser | Uses dashboards, tickets and discrepancy reports. | UC-11, UC-12, UC-14 |
| RE-03 | AdminUser | Manages user roles and permissions. | UC-13 |
| RE-04 | FinanceOfficer | Reviews employee payslip discrepancy reports. | UC-14 |
| RE-05 | Role | Groups permissions assignable to users. | UC-13 |
| RE-06 | Permission | Identifies one system access right. | UC-13, UC-15 |
| RE-07 | Session | Tracks authenticated activity and session expiry. | UC-15 |
| RE-08 | AuthService | Authenticates credentials and creates sessions. | UC-15 |
| RE-09 | Dashboard | Combines attendance, requests, notices and upcoming leave. | UC-11 |
| RE-10 | SupportTicket | Stores an IT issue and ticket number. | UC-12 |
| RE-11 | PayslipRecord | Identifies the payslip being disputed. | UC-14 |
| RE-12 | DiscrepancyReport | Reports an incorrect payslip earning or deduction. | UC-14 |
| RE-13 | DocumentLibrary | Finds authorized company documents. | UC-19 (FR-13) |
| RE-14 | Document | Stores downloadable document metadata. | UC-19 (FR-13) |
| KE-01 | Employee | Views profiles, assets, tickets and company content. | UC-16 – UC-20 |
| KE-02 | ITStaff | Confirms asset returns and posts ticket updates. | UC-16, UC-17 |
| KE-03 | EmployeeProfile | Stores personal and contact information. | UC-20 |
| KE-04 | EmergencyContact | Stores an employee’s emergency contact. | UC-20 |
| KE-05 | EmployeeRequest {abstract} | Shares request status and creation time. | UC-16, UC-17 |
| KE-06 | AssetReturnRequest | Requests return of a borrowed asset. | UC-16 |
| KE-07 | AssetLoan | Tracks one borrowing and its due date. | UC-16 |
| KE-08 | ITAsset | Stores equipment details and current status. | UC-16 |
| KE-09 | ITTicket | Supports IT ticket status and update tracking. | UC-17 |
| KE-10 | TicketUpdate | Stores an IT-authored message and status. | UC-17 |
| KE-11 | CompanyAnnouncement | Stores an announcement and publication details. | UC-18 |
| KE-12 | DocumentCenter | Searches authorized company documents. | UC-19 |
| KE-13 | CompanyDocument | Checks document access and supports downloading. | UC-19 |

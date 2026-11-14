# Component Diagram

- `Software_Architecture_Component_Diagram.pdf` – page 1: UML component diagram (components, assigned classes, provided interfaces as lollipops, required interfaces as sockets, assembly connectors, dependencies, external systems, layers); page 2: interface definitions with every operation's parameters and return types.
- `Software_Architecture_Component_Diagram.drawio` – native draw.io file (two pages), editable at app.diagrams.net.

## Interface summary

| Interface | Provided by | Required by | Operations |
|---|---|---|---|
| IAccessControl | CO1 | CO2, CO3, CO4, CO6 | login(username: String, password: String): Session [0..1]<br>logout(sessionId: String): void<br>isSessionExpired(sessionId: String): boolean<br>hasPermission(u: UserAccount, code: String): boolean |
| IEmployeeRecords | CO1 | CO2, CO3, CO5 | getProfile(employeeId: String): Employee<br>getDirectManager(employeeId: String): Employee [0..1]<br>getDirectReports(managerId: String): List<Employee><br>getDepartmentEmployees(departmentId: String): List<Employee><br>applyProfileChange(employeeId: String, field: String, newValue: String): void |
| IEmployeeDirectory | CO1 | ONE client only | search(keyword: String, field: SearchField): List<Employee><br>getPublicProfile(employeeId: String): Employee |
| IAccountAdministration | CO1 | ONE client only | createAccount(e: Employee): UserAccount<br>assignRole(u: UserAccount, r: Role): void<br>removeRole(u: UserAccount, r: Role): void<br>updatePermissions(r: Role, p: List<Permission>): void |
| INotification | CO2 | CO3, CO5, CO6 | notify(to: Employee, type: NotificationType, msg: String, sourceRef: String): Notification<br>getUnreadNotifications(employeeId: String): List<Notification><br>markAsRead(notificationId: String): void |
| IAnnouncement | CO2 | CO4, CO5 | publishAnnouncement(title: String, body: String, scope: AudienceScope): Announcement<br>getLatestAnnouncements(e: Employee, limit: int): List<Announcement> |
| IRequestLifecycle | CO3 | CO5, CO6 | submit(r: Request): boolean<br>cancel(requestId: String): boolean<br>getStatus(requestId: String): RequestStatus<br>updateStatus(requestId: String, newStatus: RequestStatus, by: UserAccount): void<br>getRequestHistory(employeeId: String, status: RequestStatus): List<Request><br>requestProfileChange(employeeId: String, field: String, newValue: String): ProfileChangeRequest<br>validateAttachment(a: Attachment, maxBytes: long): boolean |
| ILeaveManagement | CO3 | CO5 | getLeaveBalance(employeeId: String, type: LeaveType): LeaveBalance<br>getUpcomingLeave(employeeId: String): List<LeaveRequest><br>deductLeave(employeeId: String, type: LeaveType, days: double): boolean |
| IApproval | CO3 | CO4, CO6 | getPendingApprovals(approverId: String): List<Request><br>approveRequest(r: Request, comment: String): ApprovalDecision<br>rejectRequest(r: Request, reason: String): ApprovalDecision<br>recordDecision(r: Request, outcome: DecisionType, comment: String, by: Employee): ApprovalDecision |
| IAssetManagement | CO3 | ONE client only | isAvailable(assetId: String): boolean<br>processAssetRequest(r: AssetRequest, approved: boolean): ApprovalDecision<br>extendDueDate(loanId: String, newDate: Date): void<br>confirmReturn(loan: AssetLoan, condition: String): void |
| ISupportTicket | CO3 | CO4 | createTicket(category: IssueCategory, description: String, by: Employee): ITSupportTicket<br>updateTicket(t: ITSupportTicket, status: RequestStatus, message: String): TicketUpdate<br>getLatestUpdate(ticketNumber: String): TicketUpdate [0..1] |
| IDocumentCenter | CO4 | ONE client only | search(keyword: String, category: DocumentCategory): List<Document><br>getAccessibleDocuments(u: UserAccount): List<Document><br>download(documentId: String, u: UserAccount): byte[] |
| IONEAI | CO4 | ONE client only | ask(e: Employee, question: String): AIResponse<br>escalateToSupport(q: AIQuery, confirmedBy: Employee): ITSupportTicket |
| IHRPublishing | CO4 | ONE client only | publishDocument(d: Document): boolean<br>publishAnnouncement(title: String, body: String, scope: AudienceScope): Announcement<br>verifyProfileChange(r: ProfileChangeRequest, approved: boolean): ApprovalDecision |
| IDashboard | CO5 | ONE client only | getPendingRequests(employeeId: String): List<Request><br>getUpcomingLeave(employeeId: String): List<LeaveRequest><br>getUnreadNotifications(employeeId: String): List<Notification><br>getLatestAnnouncements(limit: int): List<Announcement><br>refresh(): void |
| IAttendance | CO5 | ONE client only | getAttendanceSummary(employeeId: String, from: Date, to: Date): AttendanceSummary<br>getRecords(employeeId: String, from: Date, to: Date): List<AttendanceRecord> |
| IExpenseClaims | CO6 | ONE client only | addItem(claimId: String, item: ExpenseItem): void<br>getTotalAmount(claimId: String): double<br>reviewClaim(c: ExpenseClaim, outcome: DecisionType, comment: String): ApprovalDecision |
| IPayslipEnquiry | CO6 | ONE client only | fetchPayslips(employeeId: String, period: String): List<Payslip><br>getCachedPayslips(employeeId: String, now: DateTime): List<Payslip><br>resolveDiscrepancy(r: PayslipDiscrepancyReport, response: String): void |
| IExternalConnection | CO6 | CO5 | testConnection(): boolean<br>getLastSuccessfulSync(): DateTime |
| IERPPayslipAPI | ERP System | CO6 | getPayslips(employeeId: String, period: String): List<Payslip> |
| IAttendanceAPI | Attendance System | CO5 | getRecords(employeeId: String, from: Date, to: Date): List<AttendanceRecord> |

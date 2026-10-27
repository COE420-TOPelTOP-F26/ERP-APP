# Record of modifications

The 56 individual class entries were consolidated into 44 approved classes and 14 enumerations. The main modifications are recorded below.

- Merged duplicate employees and profiles into Employee; combined ticket, payslip, document and announcement classes under consistent names.
- Merged EmployeeRequest and ServiceRequest into Request. Combined borrow, extension and return requests into AssetRequest with a request type; retained AssetLoan to track borrowing history.
- Generalized Receipt into Attachment and RequestStatusChange into AuditEntry. Added ProfileChangeRequest, NotificationService, IntegrationAdapter and AttendanceAdapter; renamed ERPConnector to PayrollAdapter.
- Removed the separate SystemUser hierarchy and AuthService. Employee specializations now own staff responsibilities, while UserAccount, Role and Permission handle authentication and access.
- Checked inheritance, attributes, methods and multiplicities. Staff specialize Employee, six request types specialize Request, and attendance/payroll adapters specialize IntegrationAdapter. Each request has one submitter and an audit history; roles and permissions are shared. Manager, HR, Finance and IT decisions are assigned to the responsible classes.

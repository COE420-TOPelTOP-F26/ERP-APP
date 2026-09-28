# Use Cases — ONE System

The following are the 20 individual use case contributions and the approved use cases represented in the overall team diagram.

| ID | Use case | Primary actor | Short description | Contributor |
|---|---|---|---|---|
| UC-01 | Submit Leave Request | Employee | Submit a leave request with a leave type and dates. | Tala Abed |
| UC-02 | Approve Leave Request | Manager | Review a pending request and approve or reject it. | Tala Abed |
| UC-03 | Submit Travel Expense Claim | Employee | Submit an expense claim with an amount, category, and receipt. | Tala Abed |
| UC-04 | Request IT Asset | Employee | Request to borrow an IT asset for a specified period. | Tala Abed |
| UC-05 | Ask ONEAI a Question | Employee | Ask a question and receive an answer based on approved company documents. | Tala Abed |
| UC-06 | View Attendance Summary | Employee | View recorded entry and exit times and total hours worked. | Nadine Alameldin |
| UC-07 | Search Employee Directory | Employee | Search for a colleague by name, department, or position. | Nadine Alameldin |
| UC-08 | Publish Company Announcement | HR Department | Create and publish an announcement for employees. | Nadine Alameldin |
| UC-09 | View Payslip and Salary Information | Employee | View available salary information and payslips retrieved from the ERP system. | Nadine Alameldin |
| UC-10 | View Request History | Employee | Review previously submitted requests and their statuses. | Nadine Alameldin |
| UC-11 | View Personalized Dashboard | Employee | View attendance information, pending requests, notifications, and upcoming leave. | Razan El Gendy |
| UC-12 | Submit IT Support Request | Employee | Report a technical issue and receive a support ticket number. | Razan El Gendy |
| UC-13 | Manage User Roles and Permissions | System Administrator | Assign, update, or remove user roles and permissions. | Razan El Gendy |
| UC-14 | Report Payslip Discrepancy | Employee | Report an incorrect earning or deduction to Finance. | Razan El Gendy |
| UC-15 | Authenticate User | Employee | Sign in with valid credentials to access authorized features. | Razan El Gendy |
| UC-16 | Return IT Asset | Employee | Request the return of a borrowed IT asset. | Kholoud Elkholy |
| UC-17 | Track IT Support Request | Employee | View a support ticket's status and latest updates. | Kholoud Elkholy |
| UC-18 | View Company Announcements | Employee | Read published company or department announcements. | Kholoud Elkholy |
| UC-19 | Search and Download Document | Employee | Find and download an authorized document or form. | Kholoud Elkholy |
| UC-20 | View Employee Profile | Employee | View authorized personal and contact information. | Kholoud Elkholy |

## Use case relationships

For an `<<extend>>` relationship, the optional use case extends the base use case. The description below states the intended direction explicitly.

| ID | Base use case | Related use case | Relationship | Justification |
|---|---|---|---|---|
| R-01 | UC-11 View Personalized Dashboard | UC-06 View Attendance Summary | `<<include>>` | The dashboard always displays attendance information. |
| R-02 | UC-09 View Payslip and Salary Information | UC-14 Report Payslip Discrepancy | `<<extend>>` | Reporting a discrepancy is optional while viewing a payslip. UC-14 extends UC-09. |
| R-03 | UC-10 View Request History | UC-17 Track IT Support Request | `<<extend>>` | Viewing detailed ticket updates is optional when the selected request is an IT support ticket. UC-17 extends UC-10. |
| R-04 | UC-05 Ask ONEAI a Question | UC-19 Search and Download Document | `<<extend>>` | After receiving an answer, the employee may choose to open or download a cited document. UC-19 extends UC-05. |
| R-05 | UC-05 Ask ONEAI a Question | UC-12 Submit IT Support Request | `<<extend>>` | If a technical question is unresolved, the employee may submit a support ticket. UC-12 extends UC-05. |

## Overall UML diagram

The team's overall use case diagram is stored in [Use_Case_Diagram/ONE_UseCase_Diagram.jpg](Use_Case_Diagram/ONE_UseCase_Diagram.jpg). It shows the ONE System boundary, the Employee, Manager, HR Department, System Administrator, and Finance Department actors, and all 20 use cases listed above.
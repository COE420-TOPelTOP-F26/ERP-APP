# Lab 3 Non-Functional Requirements

| ID | Category | Non-functional requirement | Contributor |
|---|---|---|---|
| NFR-01 | Performance | The ONE Approvals dashboard shall load within 2 seconds for a manager with up to 50 pending requests. | Tala Abed |
| NFR-02 | Security | Uploaded receipts and documents shall be encrypted at rest and accessible according to assigned roles. | Tala Abed |
| NFR-03 | Usability | During usability testing, first-time employees shall complete a leave request without training in under 90 seconds on average. | Tala Abed |
| NFR-04 | Reliability | The system shall maintain at least 99% uptime during business hours, Sunday–Thursday, 8:00 a.m.–5:00 p.m. | Tala Abed |
| NFR-05 | Scalability | The system shall support 500 concurrent users without response times increasing by more than 20% against the agreed baseline. | Tala Abed |
| NFR-06 | Robustness | If the ERP integration returns an invalid or delayed response, the application shall remain operational and display a clear error message. | Nadine Alameldin |
| NFR-07 | Availability | If the ERP connection is unavailable, the Payroll section shall display the last successfully retrieved payslip data with an indication that it may be outdated. | Nadine Alameldin |
| NFR-08 | Maintainability | The Directory, Announcements, and Payroll modules shall be independently maintainable without changes to unrelated modules. | Nadine Alameldin |
| NFR-09 | Privacy | Payslip information shall be visible only to the employee and authorized Finance or HR staff. | Nadine Alameldin |
| NFR-10 | Portability | Core application functions shall work on supported desktop browsers and mobile devices. | Nadine Alameldin |
| NFR-11 | Usability | During usability testing, first-time employees shall submit an IT support request without training within 2 minutes. | Razan El Gendy |
| NFR-12 | Performance | The personalized employee dashboard shall load within 3 seconds under normal operating conditions. | Razan El Gendy |
| NFR-13 | Robustness | An unsupported upload shall produce a clear error without crashing the application or deleting entered form data. | Razan El Gendy |
| NFR-14 | Reliability | During testing, at least 99% of valid employee requests shall be saved and retrieved without data loss. | Razan El Gendy |
| NFR-15 | Size | The system shall accept individual document and receipt uploads up to 10 MB and reject larger uploads with a clear message. | Razan El Gendy |
| NFR-16 | Auditability | The system shall record the user, date, time, and action for request submission, approval, rejection, and updates. | Kholoud Elkholy |
| NFR-17 | Session security | The system shall automatically end a session after the configured period of inactivity. | Kholoud Elkholy |
| NFR-18 | Usability | Each notification shall identify the related request, announcement, or event and provide access to its details. | Kholoud Elkholy |
| NFR-19 | Maintainability | A change to the Announcements module shall pass the Directory and Payroll modules’ existing tests without requiring changes to their source code. | Kholoud Elkholy |
| NFR-20 | Data integrity | The system shall reject incomplete or invalid requests and retain valid information entered when validation fails. | Kholoud Elkholy |
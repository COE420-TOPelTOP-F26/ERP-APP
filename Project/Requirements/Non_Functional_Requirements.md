# Non-Functional Requirements — ONE System

| ID | Category | Non-functional requirement | Contributor |
|---|---|---|---|
| NFR-01 | Performance | The ONE Approvals dashboard shall load within 2 seconds for a manager with up to 50 pending requests under normal operating conditions. | Tala Abed |
| NFR-02 | Security | Uploaded receipts and documents shall be encrypted at rest and accessible only to users whose assigned roles permit access. | Tala Abed |
| NFR-03 | Usability | In a usability test, first-time employees shall complete a leave request without training in an average of under 90 seconds. | Tala Abed |
| NFR-04 | Reliability | The system shall achieve at least 99% availability during business hours, Sunday through Thursday, 8:00 a.m. to 5:00 p.m. | Tala Abed |
| NFR-05 | Scalability | The system shall support 500 concurrent users with response times no more than 20% higher than the agreed baseline load test. | Tala Abed |
| NFR-06 | Robustness | If the ERP integration returns an unexpected, delayed, or invalid response, the application shall remain operational and display a clear error message. | Nadine Alameldin |
| NFR-07 | Availability | If the ERP connection is temporarily unavailable, the Payroll section shall show the last successfully retrieved payslip data and indicate that it may be outdated. | Nadine Alameldin |
| NFR-08 | Maintainability | The Directory, Announcements, and Payroll modules shall have separate components and interfaces so a change within one module does not require changes to an unrelated module. | Nadine Alameldin |
| NFR-09 | Privacy | Payslip and payroll information shall be accessible only to the employee concerned and authorized Finance or HR personnel. | Nadine Alameldin |
| NFR-10 | Portability | The application's core employee functions shall work in current desktop browsers and on iOS and Android mobile browsers. | Nadine Alameldin |
| NFR-11 | Usability | In a usability test, a first-time employee shall submit an IT support request without training within 2 minutes. | Razan El Gendy |
| NFR-12 | Performance | The personalized employee dashboard shall load within 3 seconds under normal operating conditions. | Razan El Gendy |
| NFR-13 | Robustness | When a user selects an invalid or unsupported upload, the system shall display an error without crashing or clearing valid information already entered in the form. | Razan El Gendy |
| NFR-14 | Reliability | During system testing, at least 99% of valid submitted employee requests shall be saved and subsequently retrieved without data loss. | Razan El Gendy |
| NFR-15 | Upload size | The system shall accept individual document and receipt uploads up to 10 MB and reject larger files with a clear error message. | Razan El Gendy |
| NFR-16 | Auditability | The system shall record the user, date, time, and action when an employee request is submitted, approved, rejected, or updated. | Kholoud Elkholy |
| NFR-17 | Session security | The system shall automatically end a user session after 15 minutes of inactivity. | Kholoud Elkholy |
| NFR-18 | Usability | Each notification shall identify the request, announcement, or event that triggered it and provide access to its details. | Kholoud Elkholy |
| NFR-19 | Recoverability | The system shall back up employee requests and uploaded documents at least once every 24 hours and be able to restore them from the latest successful backup during a recovery test. | Kholoud Elkholy |
| NFR-20 | Data integrity | The system shall prevent incomplete or invalid requests from being submitted and preserve valid entered information when a validation error occurs. | Kholoud Elkholy |
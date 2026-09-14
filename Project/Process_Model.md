Software Process Model



We selected the Incremental Model process model for our ERP software.



The Incremental Model is appropriate for ONE-ERP App because the system consists of many modules that can be developed and delivered separately, such as leave management, attendance, expenses, approvals, IT assets, and ONEAI. The team can first develop the core functionality and then add additional modules in later increments.



This approach allows the team to produce working software early, receive feedback, identify integration problems, and improve later increments. It is also useful because some requirements may become clearer after users interact with early versions of the system.



> Development Increments



| Increment   | Main Features 

|-----------  |-------------------------------------------------------------

| Increment 1 | Login, employee profile, dashboard, and employee directory 

| Increment 2 | Leave management and attendance/office timer 

| Increment 3 | Travel expenses and approval workflows 

| Increment 4 | IT asset borrowing and IT support 

| Increment 5 | ONEAI, notifications, announcements, and document center 





> Overheads and Drawbacks



* Integration overhead: Different modules must communicate with the ERP and potentially other company systems.  
* Management: Define interfaces early and use mock APIs/data when real system access is unavailable.
* Repeated testing: Adding a new increment may affect previously developed features.  
* Management: Perform integration and regression testing after each increment.
* Changing requirements: Employees or management may request changes after seeing early versions.  
* Management: Prioritize requirements and control changes according to project scope and schedule.




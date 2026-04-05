🚀 AUTOMATING EMPLOYEE DATA USING SERVICENOW
📌 PROJECT DESCRIPTION

This project focuses on automating employee data management using ServiceNow. It eliminates manual data entry by importing employee details from an external Excel/CSV file and automatically mapping them into the system.

The project uses Import Sets and Transform Maps to move data into the sys_user table efficiently.

🎯 OBJECTIVE
Automate employee data entry
Reduce manual errors and duplication
Improve efficiency in data management
Map employee manager using reference field
Ensure accurate and structured data storage
🛠️ TECHNOLOGIES USED
ServiceNow
Import Sets
Transform Maps
GlideRecord (Scripting)
Excel / CSV
✨ KEY HIGHLIGHTS
Automated employee onboarding process
Dynamic field mapping using Transform Maps
Manager mapping using scripting logic
Bulk data processing capability
Scalable and reusable solution
🧩 PROJECT WORKFLOW
1. Prepare Excel File

Create an Excel file with the following fields:

Name
Email
Department
Manager
Manager Email
2. Load Data into ServiceNow
Go to: System Import Sets → Load Data
Upload the file
A staging table is created automatically
3. Verify Imported Data
Open the staging table
Check imported records
Use Personalize List to view fields
4. Create Transform Map
Map staging table fields to sys_user table

Field Mapping:

Name → name
Email → email
Department → department
Manager → manager
5. Manager Mapping (Reference Field)
var mgr = new GlideRecord('sys_user');
mgr.addQuery('email', source.u_manager_email);
mgr.query();
if (mgr.next()) {
    target.manager = mgr.sys_id;
}
📸 SCREENSHOTS
![Screenshot 92](https://github.com/user-attachments/assets/c27d8e49-21e8-4c5c-9788-4a95c4c6220e)

![Screenshot ss2](https://github.com/user-attachments/assets/f4988bc8-8abd-4959-9247-00bffca731f6)


![Screenshot ss3 ](https://github.com/user-attachments/assets/08ae41a8-0219-4079-920b-aaf6b68b91a3)


![Screenshot 93](https://github.com/user-attachments/assets/f00d78f0-eee4-409a-89b9-e9cdbc843a0a)

![Screenshot 95](https://github.com/user-attachments/assets/f6fe34f7-6672-44c3-88be-3b2b4172b192)

![Screenshot 94](https://github.com/user-attachments/assets/5988fd4d-374d-4085-99cb-841b798a2f73)


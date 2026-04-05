Automating Employee Data using ServiceNow
📌 Project Description

This project focuses on automating employee data management using ServiceNow. It eliminates manual data entry by importing employee details from an external Excel/CSV file and automatically mapping them into the system.

The project leverages Import Sets and Transform Maps to efficiently transfer data into the sys_user table, ensuring accuracy, consistency, and scalability.

🎯 Objective
Automate employee data entry
Reduce manual errors and duplication
Improve efficiency in HR data management
Map employee manager using reference fields
Ensure accurate and structured data storage
🛠️ Technologies Used
ServiceNow
Import Sets
Transform Maps
GlideRecord (Server-side scripting)
Excel / CSV file
✨ Key Highlights
->Fully automated employee onboarding process
-> Smart field mapping using Transform Maps
-> Dynamic manager assignment using scripting
-> Bulk data processing with high efficiency
-> Real-time data transformation into sys_user table
🧩 Project Workflow
1. Prepare Excel File

Create an employee data file with the following fields:

Name
Email
Department
Manager
Manager Email
2. Load Data into ServiceNow
Navigate to:
System Import Sets → Load Data
Upload the Excel/CSV file
A staging table (e.g., Import Employee5) is automatically created
3. Verify Imported Data
Open the staging table
Check all records
Use Personalize List to view required fields
4. Create Transform Map
Define mapping between staging table and target table (sys_user)
Field mapping:
Source Field	Target Field
u_name	name
u_email	email
u_department	department
u_manager_email	manager (reference)
5. Manager Mapping (Reference Field)

The manager field is a reference field, so it must map to an existing user record.

var mgr = new GlideRecord('sys_user');
mgr.addQuery('email', source.u_manager_email);
mgr.query();
if (mgr.next()) {
    target.manager = mgr.sys_id;
}
6. Execute Transformation
Run the Transform Map
Data is inserted into the sys_user table
Verify transformation logs for success or errors
7. Validate Output
Check newly created user records
Confirm correct mapping of:
Name
Email
Department
Manager
Ensure no duplicate or incorrect entries
![Screenshot 92](https://github.com/user-attachments/assets/c27d8e49-21e8-4c5c-9788-4a95c4c6220e)

![Screenshot ss2](https://github.com/user-attachments/assets/f4988bc8-8abd-4959-9247-00bffca731f6)
![Screenshot ss3 ](https://github.com/user-attachments/assets/08ae41a8-0219-4079-920b-aaf6b68b91a3)


![Screenshot 93](https://github.com/user-attachments/assets/f00d78f0-eee4-409a-89b9-e9cdbc843a0a)

![Screenshot 95](https://github.com/user-attachments/assets/f6fe34f7-6672-44c3-88be-3b2b4172b192)

![Screenshot 94](https://github.com/user-attachments/assets/5988fd4d-374d-4085-99cb-841b798a2f73)


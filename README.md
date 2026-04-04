# 🚀 Automating Employee Data using ServiceNow

## 📌 Project Description
This project focuses on automating employee data management using ServiceNow. It eliminates manual data entry by importing employee details from an Excel file and automatically mapping them into the system.

The project uses Import Sets and Transform Maps to move data into the **sys_user** table efficiently.

---

## 🎯 Objective
- Automate employee data entry  
- Reduce manual errors  
- Improve data management efficiency  
- Map employee manager using reference field  

---

## ⚙️ Technologies Used
- ServiceNow  
- Import Sets  
- Transform Maps  
- Excel (CSV file)  

---

## 🧩 Project Workflow

### 1. Prepare Excel File
Created an Excel sheet with the following fields:
- Name  
- Email  
- Department  
- Manager Email  

---

### 2. Load Data into ServiceNow
- Opened **System Import Sets → Load Data**  
- Uploaded the Excel file  
- Created a staging table: `Import Employee`  

---

### 3. Verify Imported Data
- Viewed the imported data in the import table  
- Used **Personalize List** to display required fields  

---

### 4. Create Transform Map
- Mapped staging table fields to the **User (sys_user)** table  
- Field mappings:
  - Name → name  
  - Email → email  
  - Department → department  

---

### 5. Manager Field Mapping (Reference Field)
Used a script to map the manager based on email:

```javascript
var mgr = new GlideRecord('sys_user');
mgr.addQuery('email', source.u_manager_email);
mgr.query();
if (mgr.next()) {
    target.manager = mgr.sys_id;
}
<img width="1920" height="1080" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/f00d78f0-eee4-409a-89b9-e9cdbc843a0a" /><img width="1920" height="1080" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/f6fe34f7-6672-44c3-88be-3b2b4172b192" />
<img width="1920" height="1080" alt="Screenshot (94)" src="https://github.com/user-attachments/assets/5988fd4d-374d-4085-99cb-841b798a2f73" />


# 🚀 Automating Employee Data using ServiceNow

## 📌 Abstract
This project focuses on automating employee data management using ServiceNow. It eliminates manual data entry by importing employee details from Excel/CSV files into the system. Using Import Sets and Transform Maps, data is processed efficiently and stored in the sys_user table. The system improves accuracy, reduces time, and maintains proper relationships such as employee-manager hierarchy.

---

## 📖 Introduction

### 🔴 Problem Statement
Manual employee data entry leads to errors, duplication, and inefficiency. Managing relationships like managers becomes complex and inconsistent.

### 🎯 Objectives
- Automate employee data import  
- Reduce manual errors  
- Improve data consistency  
- Maintain employee-manager relationships  

---

## 📚 Literature Review
Traditional systems rely on manual entry or spreadsheets, which:
- Are time-consuming  
- Lack validation  
- Do not handle relational data efficiently  

Modern platforms like ServiceNow provide:
- Automation tools  
- Data transformation features  
- Scalable cloud solutions  

---

## ⚙️ Methodology

1. Prepare dataset (Excel/CSV)  
2. Upload using Import Sets  
3. Create staging table  
4. Configure Transform Map  
5. Map fields to sys_user table  
6. Use script for manager mapping  
7. Run transform and validate data  

---

## 🛠️ Implementation

### Tools Used
- ServiceNow  
- Excel / CSV  
- Transform Maps  
- GlideRecord scripting  

### Key Implementation
- Import employee data  
- Map fields automatically  
- Script to map manager reference  
- Use dot-walking for related fields  

---

## 📊 Results

- Employee records successfully imported  
- Manager mapping works correctly  
- Reduced manual effort  
- Improved accuracy  

---

## 🎯 Conclusion
The project successfully automates employee data management using ServiceNow. It reduces manual work, improves data accuracy, and ensures proper relationship mapping.

---

## 🔮 Future Scope
- Integration with HR systems  
- Real-time data updates  
- Advanced validation rules  
- Dashboard for analytics  

---

## 📚 References
- ServiceNow Documentation  
- Course materials  
- Academic resources on automation systems  

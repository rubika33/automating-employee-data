# Implementation

The project is implemented using ServiceNow Import Sets and Transform Maps.

Steps:
- Upload Excel file  
- Create staging table  
- Map fields to sys_user  
- Add script for manager mapping  
- Execute transform  

Script used:
var mgr = new GlideRecord('sys_user');
mgr.addQuery('email', source.u_manager_email);
mgr.query();
if (mgr.next()) {
    target.manager = mgr.sys_id;
}

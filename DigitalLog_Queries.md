## Digital Log SQL Queries
- ```SELECT * FROM ia_schema.sys_resources ORDER BY resource_id DESC;```

- ```SELECT status, user_active, * FROM ia_schema.sys_users AS U INNER JOIN ia_schema.sys_user_roles AS UR ON UR.User_id = U.user_id WHERE UR.role_id = 1 OR UR.role_id = 1067;```

- ```SELECT * FROM ia_schema.sys_roles;```
- ```SELECT * FROM ia_schema.sys_user_roles;```
- ```SELECT * FROM ia_schema.sys_role_resources;```
- ```SELECT * FROM ia_schema.sys_roles_modules;```
- ```SELECT * FROM ia_schema.sys_modules;```

- SELECT * FROM ia_schema.sys_users;

SELECT * FROM ia_schema.tbl_checklist WHERE checklist_name LIKE '%PLANT 2 Shift LogBook%'; -- 702
SELECT * FROM ia_schema.tbl_checklist WHERE checklist_name LIKE '%PLANT 1 Shift LogBook%'; -- 699

SELECT * FROM ia_schema.tbl_checklist_schedule LIMIT 5;
SELECT TO_TIMESTAMP(start_timestamp/1000), TO_TIMESTAMP(end_timestamp/1000), * 
FROM ia_schema.tbl_checklist_schedule WHERE checklist_id_fk = 699 ORDER BY checklist_schedule_id DESC;

SELECT * FROM ia_schema.sys_organization_holidays ORDER BY holiday_date DESC;

SELECT table_schema, table_name
FROM information_schema.tables
WHERE table_schema = 'ia_schema'
  AND table_type = 'BASE TABLE'
  AND table_name like '%%'
ORDER BY table_name;

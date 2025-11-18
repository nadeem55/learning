## Digital Log SQL Queries
- ```SELECT * FROM ia_schema.sys_resources ORDER BY resource_id DESC;```

- ```SELECT status, user_active, * FROM ia_schema.sys_users AS U INNER JOIN ia_schema.sys_user_roles AS UR ON UR.User_id = U.user_id WHERE UR.role_id = 1 OR UR.role_id = 1067;```

- ```SELECT * FROM ia_schema.sys_roles;```
- ```SELECT * FROM ia_schema.sys_user_roles;```
- ```SELECT * FROM ia_schema.sys_role_resources;```
- ```SELECT * FROM ia_schema.sys_roles_modules;```
- ```SELECT * FROM ia_schema.sys_modules;```

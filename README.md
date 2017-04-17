# Ansible role MariaDB

Version: 0.1.2

Supported OS: Ubuntu

Ansible role for MariaDB.

## Role variables

```
# Example: all privilages get granted
# mariadb_users:
#   - name: "username"
#     password: "password"
#     database: "database_name"
mariadb_users: []

# mariadb_databases:
#   - "database_name"
mariadb_databases: []

mariadb_backup_folder: /var/backup/mariadb
mariadb_enable_backup: True
```

## example

```
- hosts: all
  roles:
    - role: mariadb
      mariadb_databases:
        - my_db
      mariadb_users:
        - name: user
          password: MyVerySecretPassword
          database: my_db
```

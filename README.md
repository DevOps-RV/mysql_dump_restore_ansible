## MySql-Backup-Restore-Ansible
----------------
MySql DB/Table Dump in Source and restore in Target

### Requirements
----------------
Source DB host and Traget DB host should have password less SSH from Ansible Server

```markdown

# Role Variables
--------------

1. DB_NAME - Name of the DB or Multiple DB with Seperated by ","
2. SOURCE - Source DB hostname
3. TARGET - Target DB hostname
4. TABLE - Table Name in DB

# Dependencies
----------------
DB_NAME should be present in both SOURCE and TARGET

```

### Example Playbook
----------------
Single DB: ansible-playbook mysql_dump_restore.yml -e DB_NAME="DB1" -e SOURCE=hostame1 -e TARGET=hostname2

Multiple DB: ansible-playbook mysql_dump_restore.yml -e DB_NAME="DB1,DB2" -e SOURCE=hostame1 -e TARGET=hostname2

Single Table in DB: ansible-playbook mysql_dump_restore.yml -e DB_NAME="DB1" -e SOURCE=hostame1 -e TARGET=hostname2 -e TABLE=table1

Multiple Tables in DB: ansible-playbook mysql_dump_restore.yml -e DB_NAME="DB1" -e SOURCE=hostame1 -e TARGET=hostname2 -e TABLE="table1 table2"


### License
-------

BSD

### Author Information
------------------
Raghu Tekumudi

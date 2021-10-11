+ Create database and Log in:
```
sudo -u postgres psql
CREATE DATABASE home_project;
```

+ Create user and edit role:
```
CREATE USER home_project WITH PASSWORD 'password';

ALTER ROLE myprojectuser SET client_encoding TO 'utf8';
ALTER ROLE myprojectuser SET default_transaction_isolation TO 'read committed';
ALTER ROLE myprojectuser SET timezone TO 'UTC';

GRANT ALL PRIVILEGES ON DATABASE myproject TO myprojectuser;
```


+ Restore from dump:
```
sudo -u postgres pg_dump glsvar_database > dump.sql
psql -h localhost dbms_db dbms  < dump.sql  
```

glsvar_db
glsvar_user


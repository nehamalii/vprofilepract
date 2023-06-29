FROM mysql:8.0.33
LABEL "Project"="Vprofile"
LABEL "Author"="Neha"
ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="account"
ADD db_backup.sql docker-enrtypoint-initdb.d/db_backup.sql

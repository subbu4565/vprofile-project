FROM mysql:8.0.33
LABEL "Author"="Subbu"
LABEL "Project"="vprodb"
ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABSE="accounts"
ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql
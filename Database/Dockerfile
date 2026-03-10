FROM mysql:8.0.33
LABEL developer="abdelhamed"
ENV MYSQL_DATABASE=accounts \
    MYSQL_ROOT_PASSWORD=vprodbpass
EXPOSE 3306
ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
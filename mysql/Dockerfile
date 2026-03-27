FROM mysql:8.0
ENV MYSQL_ROOT_PASSWORD=RoboShop@1
CMD ["mysqld","--default-authentication-plugin=mysql_native_password"]
COPY *.sql /docker-entrypoint-initdb.d/

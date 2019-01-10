FROM ubuntu:bionic

MAINTAINER "fixdens" <fixdens@gmail.com>

RUN apt-get update && apt-get install -y \
        mariadb-server
VOLUME ["/etc/mysql", "/var/lib/mysql"]

WORKDIR /mysql

CMD ["mysqld"]

EXPOSE 3306

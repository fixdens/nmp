FROM ubuntu:bionic

MAINTAINER "fixdens" <fixdens@gmail.com>

RUN echo 'deb http://ftp.osuosl.org/pub/mariadb/repo/10.0/ubuntu trusty main' > /etc/apt/sources.list.d/mariadb.list && \
    apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xcbcb082a1bb943db && \
    apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y \
    mariadb-server-10.0 mariadb-client-10.0 curl gnupg && \
    apt-get install curl -y && \
    apt-get install gnupg -y \
    rm -rf /var/lib/mysql/*


VOLUME ["/etc/mysql", "/var/lib/mysql"]

WORKDIR /mysql

CMD ["mysqld"]

EXPOSE 3306

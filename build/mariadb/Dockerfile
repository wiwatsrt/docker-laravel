FROM alpine:3.4

RUN apk --update add \
  mariadb \
  mariadb-client

# This.. sets up the users and whatnot?
ADD mariadb_init.sh /mariadb_init.sh
ADD run.sh /run.sh
RUN chmod 775 *.sh

ADD my.cnf /etc/mysql/my.cnf

VOLUME  ["/var/log/mysql", "/var/lib/mysql"]

ENV TERM dumb

CMD ["sh", "run.sh"]

EXPOSE 3306
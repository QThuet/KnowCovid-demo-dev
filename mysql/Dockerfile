From mysql:latest
MAINTAINER Songjie Wang "wangso@missouri.edu"

ARG DEBIAN_FRONTEND=noninteractive
ENV MYSQL_ROOT_PASSWORD=root
ENV MYSQL_USER=covid19-user
ENV MYSQL_PASSWORD=covid19-pass
ENV MYSQL_DATABASE=covid19
#RUN apt-get -y update && apt-get -y install net-tools && apt-get -y install nano
COPY covid19.sql /docker-entrypoint-initdb.d
ENTRYPOINT ["/entrypoint.sh"]
CMD ["mysqld"]


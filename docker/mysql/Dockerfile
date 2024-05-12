FROM mysql:8.0

ENV MYSQL_DATABASE=docker_laravel \
  MYSQL_USER=admin \
  MYSQL_PASSWORD=password \
  MYSQL_ROOT_PASSWORD=password \
  TZ=Asia/Tokyo

COPY ./my.cnf /etc/my.cnf
RUN chmod 644 /etc/my.cnf
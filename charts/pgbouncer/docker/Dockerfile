FROM ubuntu:22.04
RUN apt-get update && apt install -y pgbouncer=1.16.1-1ubuntu1 postgresql-client-9.5
RUN useradd pgbouncer -b '/' -m
USER pgbouncer
ENV PG_CONFIG /etc/pgbouncer/pgbouncer.ini
RUN ls -la
RUN ls -la /etc/
RUN ls -la /etc/pgbouncer/
RUN chmod 777 /etc/pgbouncer/pgbouncer.ini
COPY run.sh /run.sh
COPY do_probe.sh /do_probe.sh
ENTRYPOINT /run.sh
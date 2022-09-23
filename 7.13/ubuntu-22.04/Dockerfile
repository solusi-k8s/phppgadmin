FROM solusik8s/php:8.1-ubuntu-22.04


LABEL Component="php" \
      Name="solusik8s/phppgadmin" \
      Version="7.13-ubuntu-22.04" \
      Release="1"
RUN apt -y update
RUN apt install -y phppgadmin
RUN	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; \
	rm -rf /var/lib/apt/lists/*
COPY ./root /
ENV DATABASE_HOST localhost
ENV DATABASE_PORT 5432
ENV DATABASE_DESC PostgreSQL
ENV DATABASE_SSLMODE allow
FROM postgres:alpine AS builder

COPY words.sql /docker-entrypoint-initdb.d/words.sql

ENV POSTGRES_HOST_AUTH_METHOD=trust

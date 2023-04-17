FROM postgres
ENV POSTGRES_HOST_AUTH_METHOD=trust
COPY . /docker-entrypoint-initdb.d/
EXPOSE 5432
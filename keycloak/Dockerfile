FROM jboss/keycloak:latest

COPY ./imports/realm-export.json /tmp/import.json

ENV KEYCLOAK_USER=admin \
    KEYCLOAK_PASSWORD=password \
    KEYCLOAK_IMPORT=/tmp/import.json \
    DB_DATABASE=keycloak \
    DB_USER=keycloak \
    DB_PASSWORD=keycloak \
    DB_ADDR=keycloak-mysql \
    DB_VENDOR=MYSQL

EXPOSE 9990
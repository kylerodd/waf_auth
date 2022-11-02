FROM jboss/keycloak:latest

COPY ./raincatcher-keycloak-theme/ /opt/jboss/keycloak/themes/raincatcher-keycloak-theme

ENV KEYCLOAK_USER=admin \
    KEYCLOAK_PASSWORD=password \
    DB_DATABASE=keycloak \
    DB_USER=keycloak \
    DB_PASSWORD=keycloak \
    DB_ADDR=keycloak-mysql \
    DB_VENDOR=MYSQL

EXPOSE 9990
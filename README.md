#### Local Keycloak instance

###### (Yes, I know we can docker compose all of this)

##### Create docker network from communication between KC and MySQL

```
$ docker network create mysql-network
```

##### run mysql

```
$ cd mysql
$ docker build -t kc-mysql .
$ docker run -d -p 3306:3306 --network mysql-network --name keycloak-mysql kc-mysql
$ cd ..
```

##### run keycloak

```
$ cd keycloak
$ docker build -t waf-keycloak .
$ docker run -d --name waf_keycloak -p 8443:8443 \
        -p 8085:8080 -p 9990:9990 \
         --network mysql-network \
        waf-keycloak
```

# keycloak-on-the-rocks
Keycloak application with spirng backend and react frontend. Single sign on, we will use postgresql as the database.

## Docker Keycloak
Run it using docker 
https://www.keycloak.org/getting-started/getting-started-docker

docker run -p 8080:8080 -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=admin quay.io/keycloak/keycloak:21.1.1 start-dev

There is a example realm in https://github.com/novomatic-tech/keycloak-examples/blob/master/examples-realm.json


## References

https://github.com/andres81/spring-boot-reactjs-keycloak-webapp
It is what i want to do as well, but its older react.

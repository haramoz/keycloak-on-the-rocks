# Weekend Fun
I am going to implement a keycloak server that integrates the google idp 

## Tech specifications:
- Keycloak server based on Wildfly
- wildfly 18
- wildfly adapter
- google idp
- dummy project jsf-demo

## jsf-demo
This project is built as the test project for the keycloak. It is deployed in the wildfly server running locally. http://localhost:8080/jsf-demo/ shows a Hello-World text. The app is right now not "AWARE" of the keycloak settings, thats why it is still accessible without authentication

## Install keycloak adapter
- Downloaded the wildfly adapter for keycloak 21. thats the oldest currently available.
- ~/Downloads/keycloak-oidc-wildfly-adapter-21.0.0$ sudo rsync -av ./bin /opt/wildfly/bin
- https://www.mastertheboss.com/keycloak/installing-keycloak-client-adapters-on-wildfly/
- adapter installation is a success. /opt/wildfly/bin$ sudo ./jboss-cli.sh --file=adapter-elytron-install-offline.cli
- Now we make our application keycloak aware by adding keycloak.json and security constraints in the web.xml
- normal login method with test1 / test123 works
- google works too!!
- recorded a video to show to work

## Notes
To represent the user add the following to the server-identities definition <secret value="QXBwbGVAMTIzIw==" />
arka/Apple...

sudo systemctl stop wildfly
sudo systemctl start wildfly

./jboss-cli.sh --file=adapter-elytron-install-offline.cli
## References
- Wildfly installation steps: https://linux.how2shout.com/install-wildfly-application-server-on-ubuntu-20-04-22-04-lts/
- build a dummy jsf project using maven for the wildfly testing https://medium.com/swlh/create-a-primefaces-jsf-project-with-maven-and-wildfly-bb695bed84c8
- keycloak with databases docker-compose ideas https://github.com/keycloak/keycloak-containers/blob/main/docker-compose-examples/keycloak-postgres-jdbc-ping.yml
- social login https://www.mastertheboss.com/keycloak/google-social-login-with-keycloak/?expand_article=1
- https://medium.com/@hasnat.saeed/install-keycloak-openid-connect-client-adapter-on-wildfly-on-ubuntu-18-04-ef98a99fc528




FROM tomcat:9.0.48-jdk11-adoptopenjdk-hotspot
EXPOSE 9080
# EN
#EXPOSE 8443
# HU
EXPOSE 9443
# EN
# COPY /target/bank##2.1.0.122.war /usr/local/tomcat/webapps/
# HU
COPY /target/bank##2.1.0.123_HU.war /usr/local/tomcat/webapps/
COPY /target/classes/application.properties /usr/local/tomcat/conf/digitalbank.properties
COPY /target/classes/keystore/digisic.p12 /usr/local/tomcat/conf/digisic.p12
COPY /target/classes/server.xml /usr/local/tomcat/conf/server.xml
HEALTHCHECK CMD curl -fail http://localhost:9080/bank/api/v1/health || exit 1

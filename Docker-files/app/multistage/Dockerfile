FROM openjdk:11 AS BUILD_IMAGE
FROM maven AS MAVEN
RUN git clone https://github.com/bakoba66/vprofile-project.git
RUN cd vprofile-project && git checkout docker && mvn install

FROM tomcat:9-jre11

RUN rm -rf /usr/local/opt/tomcat/webapps/*

COPY --from=MAVEN vprofile-project/target/vprofile-v2.war /usr/local/opt/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]

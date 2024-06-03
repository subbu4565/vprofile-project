FROM openjdk:11 AS stage
LABEL "Author"="Subbu"
LABEL "Project"="vproapp"
RUN apt update && apt install maven -y
RUN git clone https://github.com/subbu4565/vprofile-project.git
RUN cd vprofile-project && git checkout containers && mvn install

FROM tomcat:9-jre11
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=stage vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh","run"]

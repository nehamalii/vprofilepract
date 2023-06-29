FROM OPENJDK:11 AS BUILD_IMAGE
RUN apt update && apt install maven -y
RUN git clone https://github.com/nehamalii/vprofile-project.git
RUN cd vprofile-project && git checkout docker && mvn install 
FROM tomact:9-jdk21-openjdk
LABEL "Project"="Vprofile"
LABEL "Author"="Neha"
RUN rm -rf /usr/local/tomact/webapps/*
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomact/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]

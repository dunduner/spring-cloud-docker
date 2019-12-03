FROM java:8
MAINTAINER zhangning
VOLUME /tmp
#ARG JAR_FILE
#COPY /target/*.jar app.jar
COPY target/*.jar app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]

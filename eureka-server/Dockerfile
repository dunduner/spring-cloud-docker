FROM java:8
MAINTAINER zhangning
VOLUME /tmp
RUN mvn clean package docker:build
#ARG JAR_FILE
ADD target/*.jar app.jar
RUN bash -c 'touch /app.jar'
#COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]

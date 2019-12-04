FROM java:8
MAINTAINER zhangning
VOLUME /tmp
#ARG JAR_FILE
ADD target/*.jar app.jar
RUN bash -c 'touch /app.jar'
EXPOSE 8761
#COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]

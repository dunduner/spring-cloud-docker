FROM java:jre-alpine
MAINTAINER zhangning
#COPY /target/*.jar app.jar
ADD *.jar app.jar
ENTRYPOINT [ "java", "-jar", "app.jar" ]

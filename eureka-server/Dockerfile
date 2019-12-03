FROM java:jre-alpine
MAINTAINER zhangning
RUN mvn clean
RUN mvn install
#COPY /target/*.jar app.jar
ADD /target/*.jar app.jar
ENTRYPOINT [ "java", "-jar", "app.jar" ]

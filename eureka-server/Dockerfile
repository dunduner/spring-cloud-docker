FROM java:jre-alpine
MAINTAINER zhangning
RUN /bin/bash -c 'mvn clean'
RUN /bin/bash -c 'mvn install'
#COPY /target/*.jar app.jar
ADD /target/*.jar app.jar
ENTRYPOINT [ "java", "-jar", "app.jar" ]

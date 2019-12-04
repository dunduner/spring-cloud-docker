FROM java:8
MAINTAINER zhangning
VOLUME /tmp
# 安装必要的工具
RUN mkdir /opt/maven && \
    cd /opt/maven && \
    wget http://mirror.bit.edu.cn/apache/maven/maven-3/3.6.1/binaries/apache-maven-3.6.1-bin.tar.gz && \tar zvxf apache-maven-3.6.1-bin.tar.gz  && \
    tar zvxf apache-maven-3.6.1-bin.tar.gz
# 设置环境变量
ENV MAVEN_HOME /opt/maven/apache-maven-3.6.1
ENV PATH $PATH:$JAVA_HOME/bin:$CATALINA_HOME/bin:$MAVEN_HOME 
RUN source /etc/profile
RUN mvn clean package
#ARG JAR_FILE
ADD target/*.jar app.jar
RUN bash -c 'touch /app.jar'
#COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]

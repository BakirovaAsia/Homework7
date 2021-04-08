#FROM alpine:latest 
FROM openjdk:8-jre-alpine
#RUN apk add tomcat
RUN apk add --no-cache wget
#openjdk8-jre-base
#openjdk11-jre-headless
#base

#ENV JAVA_HOME /usr/lib/jvm/java-1.8-openjdk
#ENV PATH $PATH:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin

WORKDIR /usr/local/tomcat

#apache-tomcat-8.5.64.tar.gz  
#apache-tomcat-9.0.44

RUN wget https://mirrors.nav.ro/apache/tomcat/tomcat-8/v8.5.64/bin/apache-tomcat-8.5.64.tar.gz   -O /tmp/tomcat.tar.gz \
    && cd /tmp && tar xvfz /tmp/tomcat.tar.gz \
    && cp -Rv /tmp/apache-tomcat-8.5.64/* /usr/local/tomcat/ \
    && rm -rf /tmp/* \
            /usr/local/tomcat/webapps/docs/* \
            /usr/local/tomcat/webapps/examples/*

WORKDIR /usr/local/pack

RUN pwd && ls -la && \ 
#cp -rf /tmp/* /usr/local/tomcat/webapps/ \
#    && rm -rf /tmp/


EXPOSE 8080
CMD /usr/local/tomcat/bin/catalina.sh run
FROM alpine:latest

#RUN apk add tomcat9
RUN apk add \
#openjdk8-jre-base
openjdk11-jre-headless
#base

ENV JAVA_HOME /usr/lib/jvm/java-1.8-openjdk
ENV PATH $PATH:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin

WORKDIR /usr/local/tomcat

RUN wget https://mirrors.nav.ro/apache/tomcat/tomcat-9/v9.0.44/bin/apache-tomcat-9.0.44.tar.gz   -O /tmp/tomcat.tar.gz \
    && cd /tmp && tar xvfz /tmp/tomcat.tar.gz \
    && cp -Rv /tmp/apache-tomcat-9.0.44/* /usr/local/tomcat/

#RUN pwd && ls -la

EXPOSE 8080
CMD /usr/local/tomcat/bin/catalina.sh run
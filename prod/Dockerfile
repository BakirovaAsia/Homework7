FROM alpine:latest

WORKDIR /usr/local/tomcat

RUN wget https://mirrors.nav.ro/apache/tomcat/tomcat-9/v9.0.44/bin/apache-tomcat-9.0.44.tar.gz   -O /tmp/tomcat.tar.gz \
    && cd /tmp && tar xvfz /tmp/tomcat.tar.gz \
    && cp -Rv /tmp/apache-tomcat-9.0.44/* /usr/local/tomcat/

RUN pwd && ls -la

EXPOSE 8080
CMD /usr/local/tomcat/bin/catalina.sh run
FROM alpine:latest

RUN mkdir -p /usr/local/tomcat \
    && wget https://mirrors.nav.ro/apache/tomcat/tomcat-9/v9.0.44/bin/apache-tomcat-9.0.44-deployer.tar.gz -O /tmp/tomcat.tar.gz \
    && cd /tmp && tar xvfz /tmp/tomcat.tar.gz \
    && cp -Rv /tmp/apache-tomcat-9.0.44-deployer/* /usr/local/tomcat/

EXPOSE 8080
CMD /usr/local/tomcat/bin/catalina.sh run
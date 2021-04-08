FROM ubuntu:latest

RUN apt-get update \
    && apt-get install maven -y \
    && apt-get install git -y

WORKDIR /usr/local/
RUN git clone https://github.com/jonbos/CaucusCalculator.git
WORKDIR /usr/local/CaucusCalculator/
RUN  mvn package

WORKDIR /usr/local/webapps/
RUN cp /usr/local/CaucusCalculator/target/CaucusCalculator-0.0.1-SNAPSHOT.war . \
    && cp -r /usr/local/CaucusCalculator/target/CaucusCalculator-0.0.1-SNAPSHOT ./CaucusCalculator-0.0.1-SNAPSHOT
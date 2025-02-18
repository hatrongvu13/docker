FROM jenkins/jenkins:lts

USER root

RUN apt-get update && \
    apt-get install -y openjdk-17-jdk && \
    apt-get clean;


RUN apt-get update && \
    apt-get install -y maven && \
    apt-get clean;

USER jenkins

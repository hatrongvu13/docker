FROM jenkins/jenkins:lts

USER root

# or cai dat bang cach tai tu oracle hoac adoptOpenJdk
RUN apt-get update && \
    apt-get install -y openjdk-17-jdk && \
    apt-get clean;


RUN apt-get update && \
    apt-get install -y maven && \
    apt-get clean;

USER jenkins

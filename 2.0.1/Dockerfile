FROM centos:6
MAINTAINER Jake Low <jake.low@isilon.com>

USER root

# install dev tools
RUN yum install -y wget
RUN yum upgrade -y openssl

# install java
RUN yum install -y java-1.7.0-openjdk*

RUN wget -nv http://public-repo-1.hortonworks.com/ambari/centos6/2.x/updates/2.0.1/ambari.repo -O /etc/yum.repos.d/ambari.repo

RUN yum install -y ambari-server ambari-agent

ENV JAVA_HOME /usr/lib/jvm/jre-1.7.0-openjdk.x86_64/

RUN ambari-server setup -s -j $JAVA_HOME

EXPOSE 8080 8440 8441

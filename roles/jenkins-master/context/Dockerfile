FROM jenkins/jenkins:lts

ENV JENKINS_MASTER_PORT ${JENKINS_MASTER_PORT:-8080}
ENV JENKINS_SLAVE_AGENT_PORT ${JENKINS_SLAVE_AGENT_PORT:-55555}
ENV JENKINS_VERSION ${JENKINS_VERSION:-2.60.3}
ENV JENKINS_UC ${JENKINS_UC:-"https://updates.jenkins.io"}

COPY plugins.txt ./plugins.txt
COPY *.groovy  /usr/share/jenkins/ref/init.groovy.d/

RUN install-plugins.sh plugins.txt
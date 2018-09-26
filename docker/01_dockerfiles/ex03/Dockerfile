FROM debian
LABEL maintainer="imelnych"
RUN apt-get update -y

#DEPENDENCIES
RUN apt-get install -y git wget gcc curl ca-certificates openssh-server apt-transport-https

RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && chmod 777 script.deb.sh && ./script.deb.sh && apt-get install -y gitlab-ce

RUN gitlab-ctl reconfigure

EXPOSE 443 80 22
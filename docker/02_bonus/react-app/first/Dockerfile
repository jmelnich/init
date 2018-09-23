FROM debian
LABEL maintainer="imelnych"

# prerequisites for react app
RUN apt-get update -y
RUN apt-get install -y curl gnupg
RUN curl -sL https://deb.nodesource.com/setup_9.x | bash -
RUN apt-get install -y nodejs

#ONBUILD
ONBUILD COPY hello-world /opt/app
ONBUILD WORKDIR /opt/app

###### CHECK ######
# docker build -t ft-react .
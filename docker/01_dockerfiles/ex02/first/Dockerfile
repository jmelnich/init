FROM ruby:latest
LABEL maintainer="imelnych"

RUN apt-get update -y

#DEPENDENCIES
RUN gem install rails
RUN apt-get install nodejs -y

#ONBUILD
ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed

# bundle install will work when gemfile is present
# nodejs needed for db migrate

###### CHECK ######
# from app directory, do: docker build -t (any-name) .
# docker run --rm -p 3000:3000 (any-name)
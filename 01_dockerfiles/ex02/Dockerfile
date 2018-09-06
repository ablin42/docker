FROM ruby

RUN apt-get update -y && apt-get upgrade -y && gem install rails && apt-get install nodejs -y

ONBUILD COPY ./opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN gem install bundler

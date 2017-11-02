FROM ruby:latest
RUN mkdir /usr/src/app
RUN gem install cassandra-web
CMD cassandra-web --hosts "134.171.189.10" -B "0.0.0.0:3002"

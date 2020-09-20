FROM ruby:2.6.0

EXPOSE 3000
RUN gem install bundler
RUN apt-get update && apt-get install -y nodejs
COPY . .
RUN bundle install

RUN rails db:migrate
ENTRYPOINT rails s


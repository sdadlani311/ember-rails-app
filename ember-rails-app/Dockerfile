FROM ruby:2.4.0

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs --fix-missing --no-install-recommends

RUN mkdir -p /mnt/ember-rails-app
WORKDIR /mnt/ember-rails-app

ADD Gemfile /mnt/ember-rails-app
ADD Gemfile.lock /mnt/ember-rails-app/Gemfile.lock

RUN bundle install --binstubs

ADD . /mnt/ember-rails-app




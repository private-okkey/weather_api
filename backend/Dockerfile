FROM ruby:3.4-bookworm
WORKDIR /app

RUN apt-get update \
    && apt-get install -y --no-install-recommends default-libmysqlclient-dev \
    && rm -rf /var/lib/apt/lists/*

RUN gem install rails -v "~> 8.1.0" --no-document

COPY Gemfile Gemfile.lock ./
RUN bundle install
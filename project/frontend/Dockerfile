FROM ruby:2.5


COPY requirements.txt requirements.txt
# throw errors if Gemfile has been modified since Gemfile.lock
RUN bundle config --global frozen 1

COPY Gemfile Gemfile.lock ./
RUN bundle install

EXPOSE 4701

CMD ["ruby", "app.rb"]

COPY . .

FROM ruby

RUN apt-get update && apt-get dist-upgrade -y
RUN apt-get install node -y
RUN gem install rails

# rails new weblog
# cd /weblog
# rails generate scaffold post title:string body:text

ONBUILD RUN bundle install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:populate

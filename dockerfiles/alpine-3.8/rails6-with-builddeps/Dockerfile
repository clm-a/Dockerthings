FROM clmntlxndr/ruby-over-node
RUN apk add --no-cache --virtual .gems-builddeps build-base postgresql-dev sqlite-dev libxml2-dev libxslt-dev
RUN apk add --no-cache --virtual .usual-gems-rundeps tzdata imagemagick libpq sqlite-libs git
RUN gem install pg:'~>0.20' nokogiri:'~>1.8' sqlite3 rails-i18n:'~> 5.0.0' image_processing:'~> 1.2' bindex:'~>0.5' msgpack:'~>1.2' bootsnap:'~>1.3' byebug:'~>10.0' puma:'~>3.12' bcrypt:'~>3.1' unf_ext:'~>0.0.7' --no-ri --no-rdoc
RUN gem install rails --pre

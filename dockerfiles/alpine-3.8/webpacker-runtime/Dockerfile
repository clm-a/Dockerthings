FROM clmntlxndr/rails6-with-buiddeps
RUN mkdir /app && cd /app
WORKDIR /app
ENTRYPOINT ["sh"]
EXPOSE 3035
COPY Dockerfile.rails Gemfile* /app/
COPY Dockerfile.rails vendor* /app/vendor/
RUN rm /app/Dockerfile.rails /app/vendor/Dockerfile.rails
RUN bundle check || bundle install ; exit 0
RUN apk del .gems-builddeps
COPY Dockerfile.rails package.json* yarn.lock* node_modules* /app/
RUN yarn check --integrity || yarn install ; exit 0
CMD ["./bin/webpack-dev-server"]

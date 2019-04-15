FROM clmntlxndr/rails6-with-builddeps
RUN mkdir /app && cd /app
WORKDIR /app
COPY Dockerfile Gemfile* /app/
COPY Dockerfile vendor* /app/vendor/
RUN rm /app/Dockerfile /app/vendor/Dockerfile
RUN bundle install ; exit 0
RUN apk del .gems-builddeps
COPY Dockerfile package.json* yarn.lock* node_modules* /app/
RUN yarn install ; exit 0
ENTRYPOINT ["rails"]
EXPOSE 3000
CMD ["server","-b","0.0.0.0","-p","3000"]

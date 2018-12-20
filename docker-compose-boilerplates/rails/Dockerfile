FROM clmntlxndr/rails
RUN apk add --no-cache git
COPY Gemfile /app/
COPY vendor/gems /app/vendor/gems/
COPY package.json /app/
COPY node_modules /app/node_modules
RUN bundle install --local
RUN yarn install
CMD ./bin/rails s -p 3000

FROM crystallang/crystal:0.28.0

RUN apt update && apt install -y curl wget vim

RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add -
RUN echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

RUN apt-get update && apt-get install -y yarn libc6-dev libevent-dev libpcre2-dev libpng-dev libssl-dev libyaml-dev zlib1g-dev postgresql postgresql-contrib

RUN wget https://bin.equinox.io/c/ekMN3bCZFUn/forego-stable-linux-amd64.tgz && tar xvf forego-stable-linux-amd64.tgz -C /usr/local/bin && rm forego-stable-linux-amd64.tgz

RUN wget https://nodejs.org/dist/v10.15.3/node-v10.15.3-linux-x64.tar.xz && tar xvf node-v10.15.3-linux-x64.tar.xz && cp node-v10.15.3-linux-x64/bin/node /usr/local/bin && rm node-v10.15.3-linux-x64.tar.xz

RUN git clone https://github.com/luckyframework/lucky_cli
RUN cd lucky_cli && git checkout v0.14.0 && shards install && crystal build src/lucky.cr && mv lucky /usr/local/bin

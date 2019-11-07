FROM alpine:3.10
RUN apk add --no-cache crystal shards
RUN apk add --no-cache --virtual .icr-rundeps openssl musl-dev
RUN apk add --no-cache --virtual .icr-builddeps make yaml-dev openssl-dev readline-dev
RUN git clone https://github.com/crystal-community/icr.git
RUN make -C icr -f Makefile
RUN make install -C icr -f Makefile
RUN rm -rf icr
RUN apk del .icr-builddeps
RUN icr --disable-usage-warning
CMD icr

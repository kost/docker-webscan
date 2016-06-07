FROM gliderlabs/alpine
MAINTAINER kost - https://github.com/kost

ENV VERSION_SKIPFISH 2.10b

RUN apk --update add libc-dev make gcc openssl openssl-dev pcre-dev libidn-dev && rm -f /var/cache/apk/* && \
mkdir /opt && cd /opt && wget "https://skipfish.googlecode.com/files/skipfish-$VERSION_SKIPFISH.tgz" && \
tar xvzf skipfish-$VERSION_SKIPFISH.tgz && rm -f skipfish-$VERSION_SKIPFISH.tgz && \
ln -sf skipfish-$VERSION_SKIPFISH skipfish && cd skipfish-$VERSION_SKIPFISH && \
make && \
mkdir /work && \
adduser -D -s /bin/sh user user && chown -R user /work /opt/skipfish-$VERSION_SKIPFISH

USER user

# install -m 755 skipfish /usr/local/bin/

VOLUME /work
WORKDIR /opt/skipfish

ENTRYPOINT ["/opt/skipfish/skipfish"]

CMD ["-h"]

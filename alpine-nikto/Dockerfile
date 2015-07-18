FROM gliderlabs/alpine
MAINTAINER kost - https://github.com/kost

ENV VERSION_NIKTO 2.1.5

RUN apk --update add perl openssl perl-net-ssleay && rm -f /var/cache/apk/* && \
mkdir /opt && cd /opt && wget "https://cirt.net/nikto/nikto-$VERSION_NIKTO.tar.bz2" && \
tar xvjf nikto-$VERSION_NIKTO.tar.bz2 && rm -f nikto-$VERSION_NIKTO.tar.bz2 && \
ln -sf nikto-$VERSION_NIKTO nikto && cd nikto-$VERSION_NIKTO && \
chmod 755 /opt/nikto/nikto.pl && /opt/nikto/nikto.pl -update && \
mkdir /work && \
adduser -D -s /bin/sh user user && chown -R user /work

USER user

VOLUME /work
WORKDIR /opt/nikto

ENTRYPOINT ["/opt/nikto/nikto.pl"]

CMD ["-h"]

FROM gliderlabs/alpine
MAINTAINER kost - https://github.com/kost

RUN apk --update add perl openssl perl-net-ssleay git && rm -f /var/cache/apk/* && \
mkdir /opt && cd /opt && git clone https://github.com/sullo/nikto.git nikto-git && \
ln -sf /opt/nikto-git/program /opt/nikto && cd /opt/nikto && \
chmod 755 /opt/nikto/nikto.pl && /opt/nikto/nikto.pl -update && \
mkdir /work && \
adduser -D -s /bin/sh user user && chown -R user /work

USER user

VOLUME /work
WORKDIR /opt/nikto

ENTRYPOINT ["/opt/nikto/nikto.pl"]

CMD ["-h"]

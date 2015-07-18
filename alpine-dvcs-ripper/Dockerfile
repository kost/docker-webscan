FROM gliderlabs/alpine
MAINTAINER kost - https://github.com/kost


RUN apk --update add bash perl openssl perl-io-socket-ssl perl-dbi perl-dbd-sqlite perl-lwp-protocol-https git subversion cvs mercurial bzr && rm -f /var/cache/apk/* && \
mkdir /opt && cd /opt && git clone https://github.com/kost/dvcs-ripper.git && \
chmod 755 /opt/dvcs-ripper/*pl && \
mkdir /work && \
adduser -D -s /bin/sh user user && chown -R user /work

USER user

ENV PATH /opt/dvcs-ripper:$PATH

VOLUME /work
WORKDIR /work

CMD ["cat","/opt/dvcs-ripper/README.md"]

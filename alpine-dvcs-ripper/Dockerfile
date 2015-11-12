FROM gliderlabs/alpine
MAINTAINER kost - https://github.com/kost


RUN apk --update add bash perl openssl perl-io-socket-ssl perl-dbi perl-dbd-sqlite perl-lwp-protocol-https git subversion cvs mercurial bzr perl-dev make gcc musl-dev perl-test-warn && \
rm -f /var/cache/apk/* && \
(echo y;echo o conf prerequisites_policy follow;echo o conf commit)|cpan && \
cpan -f Parallell::ForkManager Redis Algorithm::Combinatorics && \
mkdir /opt && cd /opt && git clone https://github.com/kost/dvcs-ripper.git && \
chmod 755 /opt/dvcs-ripper/*pl && \
mkdir /work && \
adduser -D -s /bin/sh user user && chown -R user /work

USER user

ENV PATH /opt/dvcs-ripper:$PATH

VOLUME /work
WORKDIR /work

CMD ["cat","/opt/dvcs-ripper/README.md"]

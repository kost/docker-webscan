FROM gliderlabs/alpine
MAINTAINER kost - https://github.com/kost

RUN apk --update add python openssl git && rm -f /var/cache/apk/* && \
mkdir /opt && cd /opt && git clone https://github.com/sqlmapproject/sqlmap.git && \
cd /opt/sqlmap && \
chmod 755 /opt/sqlmap/sqlmap.py && \
mkdir /work && \
adduser -D -s /bin/sh user user && chown -R user /work

USER user

VOLUME /work
WORKDIR /opt/sqlmap

ENTRYPOINT ["/opt/sqlmap/sqlmap.py"]

CMD ["--help"]

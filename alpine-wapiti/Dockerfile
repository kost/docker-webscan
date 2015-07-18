FROM gliderlabs/alpine
MAINTAINER kost - https://github.com/kost

ENV VERSION_WAPITI 2.3.0

RUN apk --update add python openssl py-pip py-xml && rm -f /var/cache/apk/* && \
pip install BeautifulSoup requests && \
mkdir /opt && cd /opt && \
wget "http://downloads.sourceforge.net/project/wapiti/wapiti/wapiti-$VERSION_WAPITI/wapiti-$VERSION_WAPITI.tar.gz" && \
tar xvzf wapiti-$VERSION_WAPITI.tar.gz && \
rm wapiti-$VERSION_WAPITI.tar.gz && \
cd wapiti-$VERSION_WAPITI && \
ln -sf /opt/wapiti-$VERSION_WAPITI /opt/wapiti && \
chmod 755 /opt/wapiti/bin/wapiti && \
mkdir /work && \
adduser -D -s /bin/sh user user && chown -R user /work

USER user

ENV LANG en
ENV PATH /opt/wapiti/bin:$PATH

VOLUME /work
WORKDIR /work

ENTRYPOINT ["wapiti"]

CMD ["--help"]

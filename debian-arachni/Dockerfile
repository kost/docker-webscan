FROM debian:jessie
MAINTAINER kost - https://github.com/kost

ENV VERSION_ARACHNI 1.2-0.5.7.1

RUN apt-get -qq update && \
apt-get install -yq  wget ruby bash && \
rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && \
cd /opt && \
wget https://github.com/Arachni/arachni/releases/download/v1.2/arachni-$VERSION_ARACHNI-linux-x86_64.tar.gz && \
tar xvzf arachni-$VERSION_ARACHNI-linux-x86_64.tar.gz && \
rm -f arachni-$VERSION_ARACHNI-linux-x86_64.tar.gz && \
ln -sf /opt/arachni-$VERSION_ARACHNI /opt/arachni && \
useradd -m -s /bin/sh user && \
chown -R user /work /opt/arachni-$VERSION_ARACHNI && \
echo "Success"

USER user

ENV PATH /opt/arachni/bin:$PATH

VOLUME ["/work"]
EXPOSE 9292
# WORKDIR /

ENTRYPOINT ["/opt/arachni/bin/arachni_web"]



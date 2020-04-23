FROM centos:7

USER 0
ADD https://nodejs.org/dist/v12.16.2/node-v12.16.2-linux-x64.tar.xz /tmp/nodejs.tar.xz

RUN tar -C /tmp --strip-components=1 -xvf /tmp/nodejs.tar.xz && \
    cp /tmp/bin/node /usr/local/bin/node && \
    /tmp/bin/npm install npm -g && \
    rm -rf /tmp/*

USER 1000
ENTRYPOINT ["cat"]

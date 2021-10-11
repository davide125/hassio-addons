FROM oznu/homebridge:ubuntu

# add bashio
ADD https://github.com/hassio-addons/bashio/archive/v0.13.1.tar.gz  /tmp/bashio.tar.gz
RUN apt-get update && apt-get install -y curl jq && mkdir /tmp/bashio \
    && tar zxvf \
        /tmp/bashio.tar.gz \
        --strip 1 -C /tmp/bashio \
    \
    && mv /tmp/bashio/lib /usr/lib/bashio \
    && ln -s /usr/lib/bashio/bashio /usr/bin/bashio \
    && apt-get clean \
    && rm -rf /tmp/* /var/tmp/* /var/{cache,log}/* /var/lib/apt/lists/*

ENV TZ=UTC

# Add the nice banner
ADD https://github.com/hassio-addons/addon-ubuntu-base/raw/v7.0.1/base/rootfs/etc/cont-init.d/00-banner.sh /etc/cont-init.d/

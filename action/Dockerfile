FROM python:3.14-alpine3.23

# Setup base
RUN \
    apk add --no-cache \
        bash \
        git \
    \
    && pip3 install \
        --no-cache-dir \
        --prefer-binary \
        --find-links "https://wheels.home-assistant.io/musllinux/" \
        "git+https://github.com/matthiasbalke/repository-updater.git@fix/config-writer-not-released"

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]

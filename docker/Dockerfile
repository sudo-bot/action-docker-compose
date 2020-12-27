FROM docker/compose:alpine-1.28.0-rc1

ARG RELEASE_VERSION=alpine-1.28.0-rc1

# Metadata params
ARG VCS_REF
ARG BUILD_DATE

RUN apk add --no-cache --update make bash

COPY entrypoint.sh /entrypoint.sh

# Metadata
LABEL org.label-schema.vendor="Sudo-Bot" \
    org.label-schema.url="https://github.com/docker/compose#readme" \
    org.label-schema.name="docker-compose action" \
    org.label-schema.description="docker-compose action for GitHub actions" \
    org.label-schema.version=${RELEASE_VERSION} \
    org.label-schema.vcs-url="https://github.com/docker/compose.git" \
    org.label-schema.vcs-ref=${VCS_REF} \
    org.label-schema.build-date=${BUILD_DATE} \
    org.label-schema.docker.schema-version="1.0"

ENTRYPOINT ["/entrypoint.sh"]

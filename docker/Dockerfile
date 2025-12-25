FROM alpine:3.23

# ARG RELEASE_VERSION=2

# Metadata params
ARG VCS_REF
ARG BUILD_DATE

COPY --from=docker /usr/local/libexec/docker/cli-plugins/docker-compose /usr/local/bin/docker-compose
COPY entrypoint.sh /entrypoint.sh

# Metadata
LABEL org.label-schema.vendor="Sudo-Bot" \
    org.label-schema.url="https://github.com/sudo-bot/action-docker-compose#readme" \
    org.label-schema.name="docker-compose action" \
    org.label-schema.description="docker-compose action for GitHub actions" \
    # org.label-schema.version=${RELEASE_VERSION} \
    org.label-schema.vcs-url="https://github.com/sudo-bot/action-docker-compose.git" \
    org.label-schema.vcs-ref=${VCS_REF} \
    org.label-schema.build-date=${BUILD_DATE} \
    org.label-schema.docker.schema-version="1.0" \
    \
    com.docker.extension.publisher-url="https://github.com/sudo-bot" \
    \
    org.opencontainers.image.title="docker-compose action for GitHub actions" \
    org.opencontainers.image.description="docker-compose action for GitHub actions" \
    org.opencontainers.image.authors="williamdes@wdes.fr" \
    org.opencontainers.image.url="https://github.com/sudo-bot/action-docker-compose#readme" \
    org.opencontainers.image.documentation="https://github.com/sudo-bot/action-docker-compose#readme" \
    org.opencontainers.image.source="https://github.com/sudo-bot/action-docker-compose" \
    org.opencontainers.image.vendor="sudo-bot" \
    org.opencontainers.image.licenses="MPL-2.0" \
    org.opencontainers.image.created=${BUILD_DATE} \
    #org.opencontainers.image.version=${VERSION} \
    org.opencontainers.image.revision=${VCS_REF}
    #org.opencontainers.image.ref.name="${VERSION}"

ENTRYPOINT ["/entrypoint.sh"]

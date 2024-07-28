FROM alpine:3.19.3

# ARG RELEASE_VERSION=2

# Metadata params
ARG VCS_REF
ARG BUILD_DATE

COPY --from=docker /usr/libexec/docker/cli-plugins/docker-compose /usr/bin/docker-compose
COPY entrypoint.sh /entrypoint.sh

# Metadata
LABEL org.label-schema.vendor="Sudo-Bot" \
    org.label-schema.url="https://github.com/docker/compose#readme" \
    org.label-schema.name="docker-compose action" \
    org.label-schema.description="docker-compose action for GitHub actions" \
    # org.label-schema.version=${RELEASE_VERSION} \
    org.label-schema.vcs-url="https://github.com/docker/compose.git" \
    org.label-schema.vcs-ref=${VCS_REF} \
    org.label-schema.build-date=${BUILD_DATE} \
    org.label-schema.docker.schema-version="1.0"

ENTRYPOINT ["/entrypoint.sh"]

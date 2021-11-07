FROM traefik:v2.5.3

HEALTHCHECK --start-period=30s CMD [ "traefik", "healthcheck" ]

# hadolint ignore=DL3018
RUN set -eux; \
    apk --no-cache add gettext

COPY docker-entrypoint.sh /docker-entrypoint.sh
COPY traefik.toml /var/traefik/traefik.toml

ENTRYPOINT [ "/docker-entrypoint.sh" ]
CMD [ "traefik" ]

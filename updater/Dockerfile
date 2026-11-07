# No dependencies: talks to the Docker Engine API over the mounted socket.
FROM node:22-alpine
# OCI metadata. The workflow adds version/revision on top of these labels.
# "authors" keeps the original author attribution; Bhojan is maintained by
# Ankan Mukherjee (AGPL-3.0-only, see the repository LICENSE).
LABEL org.opencontainers.image.title="Bhojan Updater" \
      org.opencontainers.image.description="Sidecar updater for Bhojan Docker deployments" \
      org.opencontainers.image.source="https://github.com/ankanz1/Bhojan" \
      org.opencontainers.image.url="https://github.com/ankanz1/Bhojan" \
      org.opencontainers.image.documentation="https://github.com/ankanz1/Bhojan#readme" \
      org.opencontainers.image.licenses="AGPL-3.0-only" \
      org.opencontainers.image.vendor="Bhojan" \
      org.opencontainers.image.maintainer="Ankan Mukherjee" \
      org.opencontainers.image.authors="Raktim Ranjit (original author), Ankan Mukherjee (maintainer)"
WORKDIR /app
COPY updater/server.js ./
USER root
EXPOSE 8080
CMD ["node", "server.js"]

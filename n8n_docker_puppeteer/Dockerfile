# filename: Dockerfile
FROM n8nio/n8n:latest

USER root

# Install Chromium and fonts; keep image lean
RUN apk add --no-cache \
    chromium \
    nss \
    freetype \
    harfbuzz \
    ttf-freefont \
    ghostscript \
  && rm -rf /var/cache/apk/*

# Run n8n as non-root for security and to match volume ownership
USER node

ENV PUPPETEER_EXECUTABLE_PATH="/usr/bin/chromium"

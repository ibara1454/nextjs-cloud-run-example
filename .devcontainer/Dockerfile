FROM mcr.microsoft.com/devcontainers/typescript-node:dev-22-bookworm

# Install tools
RUN apt-get update && apt install -y \
  tig \
  # https://cloud.google.com/sdk/docs/install?hl=ja#deb
  apt-transport-https ca-certificates gnupg curl

RUN echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | tee -a /etc/apt/sources.list.d/google-cloud-sdk.list && curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | gpg --dearmor -o /usr/share/keyrings/cloud.google.gpg && apt-get update -y && apt-get install google-cloud-cli -y

FROM codercom/code-server:latest

ENV SHELL /bin/bash

USER root
RUN apt-get update && apt-get install --no-install-recommends -y \
    default-jre-headless \
    default-jdk-headless \
    maven \
    gradle \
    && rm -rf /var/lib/apt/lists/*

USER coder 

# Install Java support extension
RUN code-server --install-extension vscjava.vscode-java-pack

ENTRYPOINT ["dumb-init", "code-server"]

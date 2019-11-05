FROM maven:3.6.2-jdk-11

ARG PROTOBUF_VERSION=3.6.1
ARG BASE_URL=https://github.com/protocolbuffers/protobuf/releases/download/v${PROTOBUF_VERSION}/

RUN mkdir -p /usr/share/protoc \
  && curl -fsSL -o /tmp/protoc-linux.zip ${BASE_URL}/protoc-${PROTOBUF_VERSION}-linux-x86_64.zip \
  && unzip /tmp/protoc-linux.zip -d /usr/share/protoc \
  && rm -f /tmp/protoc-linux.zip \
  && ln -s /usr/share/protoc/bin/protoc /usr/bin/protoc

ARG RUST_VER=1.58

FROM rust:${RUST_VER}-buster as builder
USER root
ENV LANG=C.UTF-8 \
    CARGO_HOME="/root/.cargo" \
    USER="root"

RUN mkdir -p ${CARGO_HOME}
RUN mkdir -p /app
RUN apt-get update && apt-get install -y libzmq3-dev cmake 

# Copy sources and build
WORKDIR /app

COPY . .

RUN cargo build

EXPOSE 8080

ENTRYPOINT ["cargo", "run", "--", "-s", "./networks"]

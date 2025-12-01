FROM        --platform=$TARGETOS/$TARGETARCH golang:1.25-alpine

LABEL       author="Kiyomi Fujiwara" maintainer="kiyomi@mjba.my"

RUN         apk add --update --no-cache ca-certificates tzdata \
				&& adduser -D -h /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/ash", "/entrypoint.sh" ]

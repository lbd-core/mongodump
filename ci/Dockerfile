FROM alpine:3.19

RUN apk add --no-cache bash curl tar gzip ca-certificates python3 py3-pip
RUN apk add --no-cache aws-cli
RUN apk add --no-cache mongodb-tools
WORKDIR /app
VOLUME /mongodb
COPY backup.sh /app/backup.sh
RUN chmod +x /app/backup.sh

ENTRYPOINT ["/app/backup.sh"]

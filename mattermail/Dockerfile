FROM alpine:3.9.2

RUN apk add ca-certificates && \
    mkdir -p /mattermail/data

COPY . /mattermail/

RUN chmod +x /mattermail/mattermail

CMD ["/mattermail/mattermail"]
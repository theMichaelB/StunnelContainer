FROM alpine:edge

RUN mkdir certs

COPY Docker/docker-entrypoint.sh /entrypoint.sh

RUN apk add --no-cache stunnel gnupg libressl && chmod +x /entrypoint.sh && \
 touch /var/log/stunnel.log && chmod 666 /var/log/stunnel.log 

ENTRYPOINT ["/entrypoint.sh"]
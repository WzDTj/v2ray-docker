FROM nginx:1.21.6-alpine

ARG NGINX_SERVER_NAME
ARG NGINX_SSL_CERTIFICATE
ARG NGINX_SSL_CERTIFICATE_KEY
ARG V2RAY_PORT
ARG V2RAY_WS_PATH

COPY templates /etc/nginx/templates
COPY certs /etc/nginx/certs

RUN envsubst < /etc/nginx/templates/default.conf.template > /etc/nginx/conf.d/default.conf

EXPOSE 443

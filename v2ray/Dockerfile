FROM v2ray/official

ARG V2RAY_PORT
ARG V2RAY_ID
ARG V2RAY_ALTER_ID
ARG V2RAY_WS_PATH

COPY templates /etc/v2ray/templates

RUN apk add gettext
RUN envsubst < /etc/v2ray/templates/config.json.template > /etc/v2ray/config.json

EXPOSE ${V2RAY_PORT}

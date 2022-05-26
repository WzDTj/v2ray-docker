# V2ray Docker

本项目采用 V2ray+Nginx+WS+TLS 方案。

> 需要自备域名并申请 SSL 证书

## 用法

补充 `.env` 配置文件

```
cp .env.example .env
```

将 SSL 证书放到 `./nginx/certs/` 目录下。

```
sudo docker compose build
sudo docker compose up -d
```

## ENV 配置说明

| 变量                        | 说明               |
| --------------------------- | ------------------ |
| `V2RAY_PORT`                | V2ray 端口         |
| `V2RAY_ID`                  | V2ray ID (UUID)    |
| `V2RAY_ALTER_ID`            | V2ray Alter ID     |
| `V2RAY_WS_PATH`             | V2ray Websock 路径 |
| `NGINX_SERVER_NAME`         | 服务地址           |
| `NGINX_SSL_CERTIFICATE`     | SSL 证书路径       |
| `NGINX_SSL_CERTIFICATE_KEY` | SSL 私钥路径       |

## 其他

可通过 [Online UUID Generator](https://www.uuidgenerator.net) 生成 `V2ray ID`。

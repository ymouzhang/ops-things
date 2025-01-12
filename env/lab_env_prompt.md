# lab_env

# Role
你是一名DevOps工程师，负责为实验室环境提供支持。

# 任务
## 准备环境
1. 使用 prometheus grafana pushgateway 搭建监控环境
2. 使用node_exporter 监控主机
3. 使用 docker compose 部署 prometheus grafana pushgateway
4. 要求网络互通，可以互相访问，可以外部访问
5. 在 lab_env 目录下帮我生成相关配置文件

## 解决代理问题

‵‵‵bash
sudo mkdir -p  /etc/systemd/system/docker.service.d
sudo vim /etc/systemd/system/docker.service.d//http-proxy.conf

[Service]
Environment="HTTP_PROXY=http://127.0.0.1:10808"
Environment="HTTPS_PROXY=socks5://127.0.0.1:10808"

sudo systemctl daemon-reload
sudo systemctl restart docker
```

Ref: https://blog.csdn.net/qq_51762470/article/details/138588514

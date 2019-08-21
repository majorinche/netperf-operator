20190821
使用方法：
构建：go build -o netperf-operator cmd/netperf-operator/main.go

构建docker镜像
1）设置代理
 mkdir -p /etc/systemd/system/docker.service.d
 vim /etc/systemd/system/docker.service.d/https-proxy.conf
---
[Service]
Environment="HTTPS_PROXY=172.18.163.222:80" "NO_PROXY=localhost,127.0.0.1,xxx.xxxxxx:5000"
---
 systemctl daemon-reload
 systemctl restart docker

Get https://registry-1.docker.io/v2/: net/http: request canceled while waiting for connection (Client.Timeout exceeded while awaiting headers)

代理上网还是很慢

## 运行说明
#### 1.使用docker-compose运行
```
docker-compose up -d
chmod 777 -R prometheus grafana alertmanager pushgateway blackbox_exporter
docker-compose restart
```

## Prometheus
访问地址：http://IP:9090

## Grafana
访问地址：http://IP:3000
账号: admin
密码: admin

## Alertmanager
访问地址：http://IP:9093

## Pushgateway
访问地址：http://IP:9091

## blackbox
访问地址：http://IP:9115

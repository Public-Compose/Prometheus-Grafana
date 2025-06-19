## 运行说明
#### 1.使用docker-compose运行
```
docker-compose up -d
chmod 777 -R prometheus grafana alertmanager pushgateway blackbox_exporter snmp_exporter
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

## SNMP
已有huawei交换机
访问地址：http://IP:9116
* community要与设备的snmp配置的团体名一致
* Auth、Module即为yml文件中modules、auths的名称

</br>

## 导入Grafana面板
### blackbox
* id：9965   
![9965](https://lsky-img.hzbb.top/EAFluSPqdFTVhvgii4ENaXGjGntQVKdn/2024/10/03/66fe18e8a3115.png)

### snmp_huawei
https://github.com/robotneo/networkdevice-monitor/tree/main/generator/huawei/switch
grafana.json


## 参考链接
https://github.com/robotneo/networkdevice-monitor
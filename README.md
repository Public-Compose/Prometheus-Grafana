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
华为交换机
访问地址：http://IP:9116
* prometheus/snmp目录，yml配置需要修改为对应的华为交换机ip
* snmp_exporter/conf：
    * community要与设备的snmp配置的团体名一致
    * Wei UI的Auth、Module即为yml文件中auths、modules的名称
    * 例如：
      * Target:   # 实际的华为交换机ip
      * Auth:   public_v2
      * Module:   huawei_common,huawei_core


</br>

## 导入Grafana面板
### blackbox
* id：9965   
![9965](https://lsky-img.hzbb.top/EAFluSPqdFTVhvgii4ENaXGjGntQVKdn/2024/10/03/66fe18e8a3115.png)

### snmp_huawei
https://github.com/robotneo/networkdevice-monitor/tree/main/generator/huawei/switch
grafana.json


## 参考链接
[robotneo/networkdevice-monitor: 基于Prometheus + SNMP Exporter对网络设备的监控](https://github.com/robotneo/networkdevice-monitor)
# 更新升级

网站技术日新月异，**更新升级**是维护工作之一，长时间不升级的程序，就如长时间不维护的建筑物一样，会加速老化、功能逐渐缺失直至无法使用。  

这里注意更新与升级这两词的差异（[延伸阅读](https://support.websoft9.com/docs/faq/zh/tech-upgrade.html#更新-vs-升级)），例如：  

- 操作系统打个补丁常称之为**更新**，Ubuntu16.04 变更为 Ubuntu18.04，称之为**升级**
- MySQL5.6.25-->MySQL5.6.30 常称之为**更新**，MySQL5.6->MySQL5.7 称之为**升级**

Zabbix 完整的更新升级包括：系统级更新（操作系统和运行环境）和 Zabbix 程序升级两种类型

## 系统级更新

运行一条更新命令，即可完成系统级更新：

``` shell
#For Ubuntu&Debian
apt update && apt upgrade -y

#For Centos&Redhat
yum update -y
```
> 本部署包已预配置一个用于自动更新的计划任务。如果希望去掉自动更新，请删除对应的Cron

## Zabbix 更新

如果要更新 Zabbix 的次要版本（例如，从 4.0.1 升级至 4.0.3），是非常容易的：

```
## 更新 Zabbix 所有组件
sudo apt install --only-upgrade 'zabbix.*'

## 更新 Zabbix server
sudo apt install --only-upgrade 'zabbix-server.*'

## 更新 Zabbix agent 
sudo apt install --only-upgrade 'zabbix-agent.*'
```

## Zabbix 升级

Zabbix 升级是指从低版本升到高版本，例如 3.0 to 4.0

与升级有关的详细方案，请参考官方文档：[Zabbix 升级步骤](https://www.zabbix.com/documentation/4.0/zh/manual/installation/upgrade)
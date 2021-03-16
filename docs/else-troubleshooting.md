# Troubleshooting

We collect the most common troubleshooting of using Zabbix for your reference:

> Many troubleshooting is closely related to the Server, if you can confirm troubleshooting is related to Cloud Platform, please refer to [Cloud Platform Documentation](https://support.websoft9.com/docs/faq/tech-instance.html)

#### Database service could not be started?

Insufficient disk space, insufficient memory, and configuration file errors can make database service could not be started  

It is recommended to first check through the command.

```shell
# restart mysql service
systemctl restart mysql

# view disk space
df -lh

# view memory rate
free -lh
```

#### Zabbix can't connect MySQL when modify the password of database?

Refer to [replace-database](/solution-more.md#replace-database)

#### Zabbix-server service failed?

Run the command `sudo docker logs zabbix-server` to check logs  
# Read before using

The template is only tested on the following env:

    - CentOS 7
    - Zabbix 3.2.6
    

# how to use

## install dependencies

The script rely on `jq` command to parse JSON result.

```
# jq package is available in epel repo
yum install epel-release
yum install jq
```

## config Zabbix

1. put `zabbix_templates/es_discovery.conf` in `/etc/zabbix/zabbix_agent.d/` directory in your Zabbix agent server
2. save files in `elasticsearch_mon` to directory specified in `zabbix_templates/es_discovery.conf`
3. import template `zabbix_templates/zbx_elasticsearch_templates.xml` to Zabbix server using the web console
4. assign template to hosts

# ansible-zabbix-server
Installs and configure Zabbix server.

### Requirements
None.

### Role variables
|Key|Type|Description|Default|
|:--|:---|:----------|:------|
|zabbix_server_version|String|Install version.|3.2|
|zabbix_server_web_user|String|Web server user.|nginx|
|zabbix_server_web_group|String|Web server group.|nginx|
|zabbix_server_ListenPort|Integer|Listen port number.|10051|
|zabbix_server_db_host|String|Database host.|localhost|
|zabbix_server_db_name|String|Database name.|zabbix|
|zabbix_server_db_user|String|Database user.|zabbix|
|zabbix_server_db_pass|String|Database password.|zabbix|
|zabbix_server_slack_url|String|||
|zabbix_server_slack_username|String|||

## Dependencies
+ [php](https://github.com/shomatan/ansible-php.git)
+ [mysql](https://github.com/shomatan/ansible-mysql.git)

## Example playbook
+ [firewalld](https://github.com/shomatan/ansible-firewalld.git)

```yaml
- hosts: all
  roles:
    - { role: firewalld }
    - { role: zabbix-server }
  vars:
    zabbix_server_slack_url: "https://hooks.slack.com/services/xxxxx/yyyyy/zzzzz"
    zabbix_server_slack_username: "notify-user"    
  tasks:  
    - firewalld: service=http permanent=true state=enabled immediate=true
```

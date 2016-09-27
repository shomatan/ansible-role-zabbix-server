# ansible-zabbix-server
Installs and configure Zabbix server.

### Dependencies
None.

### Role variables
|Key|Type|Description|Default|
|:--|:---|:----------|:------|
|zabbix_server_version|String|Install version.|3.0|
|zabbix_server_web_allow_hosts|Array|Allow host network.(nginx)||
|zabbix_server_ListenPort|Integer|Listen port number.|10051|
|zabbix_server_db_host|String|Database host.|localhost|
|zabbix_server_db_name|String|Database name.|zabbix|
|zabbix_server_db_user|String|Database user.|zabbix|
|zabbix_server_db_pass|String|Database password.|zabbix|

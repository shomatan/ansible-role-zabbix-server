Ansible role: Zabbix server
=========

Installs and configures Zabbix server.

Requirements
------------

None.

Role Variables
--------------

    zabbix_server_version: "3.2"

    zabbix_server_web_user: nginx
    zabbix_server_web_group: nginx

    zabbix_server_ListenPort: 10051

    # database
    zabbix_server_db_host: localhost
    zabbix_server_db_name: zabbix
    zabbix_server_db_user: zabbix
    zabbix_server_db_pass: zabbix

    # zabbix_server.conf
    zabbix_server_StartIPMIPollers: 0
    zabbix_server_AlertScriptsPath: /usr/lib/zabbix/alertscripts

    # slack
    zabbix_server_slack_url: ""
    zabbix_server_slack_username: ""

Dependencies
------------

- shomatan.repo-epel
- shomatan.php-fpm (not docker)
- shomatan.mariadb (not docker)

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: shomatan.zabbix-server }

License
-------

BSD

Author Information
------------------

Shoma Nishitateno
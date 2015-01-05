Ansible MySQL
=============

Install and configure mysql on Debian server.

Installation
------------

git submodule add git@github.com/boostmyshoporganization/ansible-mysql roles/mysql

```yaml
roles:
    - mysql
```

Configuration
-------------

```yaml
mysql:
  version: 5.6
  root_password: 123456
  variables:
    - { name: bind-address, value: 0.0.0.0 }
    - { name: server-id, value: 1 }
    - { name: max_connections, value: 200 }
    - { name: open-files-limit, value: 4096 }
    - { name: max_allowed_packet, value: 16M }
    - { name: innodb_file_per_table }
    - { name: innodb_buffer_pool_size, value: 4Go }
```
Role Name
=========
configure-network

Роль предназначена для конфигурирования сетевых интерфейсов (без маршрутов)

Requirements
------------
 
Centos 7

Role Variables
--------------

Используется список переменных вида:

```yaml
---
# defaults file for configure-network
network_interfaces_default_type: ethernet     # Тип интерфейсов по умолчанию
network_interfaces_default_state: present     # Состояние интерфейса по умолчанию
network_interfaces:     # Список интерфейса
  - { name: fsoptical, iterface_name: p1p1, ip: 10.255.252.33/30, type: "{{network_interfaces_default_type}}", state: "{{network_interfaces_default_state}}" }

# name - логическое имя интерфейса
# iterface_name: физический интерфейс
# ip: ip адрес с указанием маски в формате /30
# type - тип интерфейса
# state - состояние интерфейса
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```yaml
    - hosts: servers
      roles: 
      - { role: configure-network}
```

Author Information
------------------

Iakov Maiurov 

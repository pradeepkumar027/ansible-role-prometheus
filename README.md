Role Name
=========

Ansible Role to install prometheus on RedHat, Centos, Amazon Linux based machines

Requirements
------------

None

Role Variables
--------------

See `defaults/main.yml`

variable `prometheus_targets` need to be defined in playbook with the targets of the servers to be scraped

Example: 

prometheus_targets: "{{ groups['webservers'] }}"

Dependencies
------------

None

Example Playbook
----------------

    - name: install prometheus
      hosts: server
      vars:
        prometheus_targets: "{{ groups['webservers'] }}"
      roles:
      - pradeepkumar027.prometheus

License
-------

BSD

Author Information
------------------

Role created by Pradeep Kumar
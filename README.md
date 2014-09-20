Nova scheduler
=========

OpenStack Nova scheduler service installation

_Tested on Ubuntu Precise (12.04) and Trusty (14.04)_

Requirements
------------

A RabbitMQ server. See `rabbit_hostname`, `rabbit_username` and
`rabbit_pass` below.

Role Variables
--------------

# Other systems/serivces
* `rabbit_hostname`:  hostname/IP address where the RabbitMQ service runs.
                      Defaults to "localhost".
* `rabbit_username`:  RabbitMQ username for nova conductor.
                      It must already exist.
                      Defaults to "rabbit\_username\_default".
* `rabbit_pass`:      RabbitMQ password for nova conductor.
                      Defaults to "rabbit\_pass\_default".

# Role specific

...

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: scheduler001
      roles:
        - role: openstack-nova_scheduler
          rabbit_username: "openstack-nova"
          rabbit_pass: "{{ RABBIT_NOVA_PASS }}"

License
-------

Apache

Author Information
------------------

Davide Guerri - davide.guerri@gmail.com

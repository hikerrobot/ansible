debian_static_ip
================

This role can be used to set a static ip address.

Requirements
------------

Debian based operating system, e.g. Ubuntu. Raspberry Pi os.

Role Variables
--------------

2 variables are required for this role:
new_host_ip: the static ip address for the host
static_router: the network gateway ip address

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - debian_static_ip

A var file is required to set the required variables. See the template in the vars directory.

License
-------

BSD


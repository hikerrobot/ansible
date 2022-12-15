Role name: git-setup
=========

Allows a different ssh key to be specified for a specific domain. e.g. github.com.

Requirements
------------

Requires you to know the path of the alternative ssh key.

Role Variables
--------------

host_name: the host name. This must match the text in the git clone command.
e.g. if clone command is git clone git@cheese.com:user/ansible.git then host_name
variable must be set to cheese.com.

host_domain: The actual domain to connect to.
user: User account name.
priv_key: Path to private key. Usually in ~/.ssh/


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- name: create git config
  hosts: localhost
  vars:
    home_dir: "{{ lookup('ansible.builtin.env', 'HOME') }}"
  roles:
    - role: git-setup

License
-------

BSD

Author Information
------------------

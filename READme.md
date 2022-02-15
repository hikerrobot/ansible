# hosts file
**don't forget to copy to /etc/ansible once updated!**

# Playbook command syntax
ansible-playbook <playbook file>

## request BECOME user password
ansible-playbook <playbook file> -K

# ansible adhoc commands
https://docs.ansible.com/ansible/latest/user_guide/intro_adhoc.html


# example adhocs:
ansible localhost -m apt -a "name=sshpass state=latest" --user <user> -K --become
ansible 10.1.10.36 -a  "touch /tmp/moto" --user pi -k
ansible-playbook ./playbooks/add_static_ip_dchpcd_conf.yml -K --extra-vars="@playbooks/var_files/dhcpcd_lan.vars"
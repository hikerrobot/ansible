# Overview
A collection of playbooks and roles. some particularly useful for rasp pis :-)

## ssh-agent setup - useful for connecting to hosts remotely with Ansible
- To start ssh-agent: `eval `ssh-agent -s``
- To add a key: `ssh-add <path to private key>`
- To list identities: `ssh-add -l`
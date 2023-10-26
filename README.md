# Overview
A collection of playbooks and roles. some particularly useful for rasp pis :-)

## ssh-agent setup - useful for connecting to hosts remotely with Ansible
- To start ssh-agent: `eval `ssh-agent -s``
- To add a key: `ssh-add <path to private key>`
- To list identities: `ssh-add -l`

## Variables at runtime
- To specify variables in a file: --extra-vars "@<var file>

## Running the Raspberry Pi setup playbook
Firstly, note that tags are present in all of the roles used.
So it's a good idea to use either the pi0, pi4 tags or specify the tagged roles (--tags tagged).

Kind of obvious, but if you want to setup a pi4 how I do then specify the pi4 tag.
And the same goes for a pi0.

## Issues with Ansible Galaxy NG
Some of the roles used within this repository are failing due to issues with changes to Ansible Galaxy,
notably because major changes have been made to Galaxy.

One of the roles to suffer is one of Jeff Geerlings, he's posted a [blog](https://www.jeffgeerling.com/blog/2023/ansible-galaxy-error-unable-compare-role-versions) about it which contains the workaround.
I utilise his docker roles, to get docker installed onto the Raspberry Pi.

For additional convenience I've created the requirements.yml which Jeff mentions in his blog.
It is in the playbooks directory. Note that the role names match those used in my pi-docker playbook so you can use that to install docker.
I have found though that docker-compose fails to install, due to Python issues.
Oh well, when it rains it pours!

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
Ansible Role: cadvisor-cadvisor-docker
----------------------

[![Build Status](https://travis-ci.org/teknique/ansible-role-cadvisor-docker.svg?branch=master)](https://travis-ci.org/teknique/ansible-role-cadvisor-docker)

Ansible role that installs cadvisor-docker, cadvisor-docker-compose and all required dependencies on Debian and Ubuntu.


## Supported Operating Systems

- Debian 9+
- Ubuntu 16.04+ (untested)

## Requirements

- Ansible 2.4+

## Role Variables

See `./defaults/main.yml` for configurable variables and their defaults

## Example playbook

    ---
    - name: Example play
      hosts: all
      roles:
        - { role: cadvisor-docker }

## Example playbook (with some optional vars set)

    ---
    - name: Example play with some optional vars set
      hosts: all
      roles:
        - { role: cadvisor-docker,
            cadvisor_docker_version: v0.28.3,
            cadvisor_docker_expose_port: 10000
          }

## Add as a submodule to your playbook repo

    git submodule add https://github.com/teknique/ansible-role-cadvisor-docker.git roles/cadvisor-docker

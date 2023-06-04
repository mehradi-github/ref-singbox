# Installing sing-box via Ansible
Installing [sing-box](https://github.com/SagerNet/sing-box) on Linux via [Ansible](https://docs.ansible.com/ansible/latest/index.html)

Ansible automates the management of remote systems and controls their desired state. more details [Automation with Ansible](https://github.com/mehradi-github/ref-ansible#automation-with-ansible).


- [Installing sing-box via Ansible](#installing-sing-box-via-ansible)
  - [Requirments](#requirments)
    - [Installing Ansible](#installing-ansible)
    - [Setting configuration](#setting-configuration)
  - [Installing sing-box on Server](#installing-sing-box-on-server)
  - [Installing sing-box on Client](#installing-sing-box-on-client)
## Requirments
### Installing Ansible
Ansible automates the management of remote systems and controls their desired state. [[Installing Ansible on Ubuntu](https://github.com/mehradi-github/ref-ansible#installing-ansible-on-ubuntu)]
### Setting configuration
## Installing sing-box on Server

-k, --ask-pass: ask for connection password

-K, --ask-become-pass: ask for privilege escalation password

```sh
cd ./src
ansible-playbook ./install-playbook.yaml -t servers 

```

## Installing sing-box on Client
```sh
cd ./src
ansible-playbook ./install-playbook.yaml -t clients

```


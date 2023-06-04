# Installing sing-box via Ansible
Installing [sing-box](https://github.com/SagerNet/sing-box) on Linux via [Ansible](https://docs.ansible.com/ansible/latest/index.html)

Ansible automates the management of remote systems and controls their desired state. more details [Automation with Ansible](https://github.com/mehradi-github/ref-ansible#automation-with-ansible).


- [Installing sing-box via Ansible](#installing-sing-box-via-ansible)
  - [Installing Ansible](#installing-ansible)
  - [Linux Server Installation](#linux-server-installation)
  - [Linux Client Installation](#linux-client-installation)

## Installing Ansible
Ansible automates the management of remote systems and controls their desired state. [[Installing Ansible on Ubuntu](https://github.com/mehradi-github/ref-ansible#installing-ansible-on-ubuntu)]
## Linux Server Installation

-k, --ask-pass: ask for connection password

-K, --ask-become-pass: ask for privilege escalation password

```sh
ansible-playbook ./install-playbook.yaml -t servers 

```

## Linux Client Installation
```sh
ansible-playbook ./install-playbook.yaml -t clients

```


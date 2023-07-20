# Installing sing-box via Ansible
Installing [sing-box](https://github.com/SagerNet/sing-box) on Linux via [Ansible](https://docs.ansible.com/ansible/latest/index.html)

Ansible automates the management of remote systems and controls their desired state. more details [Automation with Ansible](https://github.com/mehradi-github/ref-ansible#automation-with-ansible).


- [Installing sing-box via Ansible](#installing-sing-box-via-ansible)
  - [Requirments](#requirments)
    - [Installing Ansible](#installing-ansible)
    - [Adding hosts](#adding-hosts)
  - [Installing sing-box on Server](#installing-sing-box-on-server)
  - [Installing sing-box on Client](#installing-sing-box-on-client)
## Requirments
### Installing Ansible
Ansible automates the management of remote systems and controls their desired state. [[Installing Ansible on Ubuntu](https://github.com/mehradi-github/ref-ansible#installing-ansible-on-ubuntu)]
### Adding hosts
```sh
# Download project and cd to project dir

vi ./src/hosts
# Changing SERVER-IP,USER and PORT
[servers]
SERVER-IP ansible_user=USER ansible_port=PORT
```
## Installing sing-box on Server

```sh
vi ./src/roles/server-sing-box/vars/main.yml
# Changing port and SNI
listen_port: 443
server_name: 'example.com'

cd ./src
ansible-playbook ./install-playbook.yaml -t servers 

```
-k, --ask-pass: ask for connection password

-K, --ask-become-pass: ask for privilege escalation password


## Installing sing-box on Client
```sh
vi src/roles/client-sing-box/vars/main.yml
# Changing below vars based on server info
server_ipv4: 'a'
uuid: 'b'
server_name: 'c'
public_key: 'd'
short_id: 'e'

cd ./src
ansible-playbook ./install-playbook.yaml -t clients

```


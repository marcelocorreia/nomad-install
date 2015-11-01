# nomad-install

Installs [Hasicorp's Nomad] (https://nomadproject.io)



## Role Variables
```yml

---
nomad:
  version: 0.1.2
  arch: amd64

install:
  dir : /usr/local/bin
  download_location: https://dl.bintray.com/mitchellh/nomad

```


Example Playbook
----------------
```yml

---
- hosts: local
  sudo: true
  gather_facts: true

  roles:
    - marcelocorreia.nomad-install

  vars_files:
    - ../vars/tardis.yml

```

License
-------

MIT

Author Information
------------------
Some useful stuff at:
  - [https://github.com/marcelocorreia](https://github.com/marcelocorreia)
  - [https://galaxy.ansible.com/list#/users/15516](https://galaxy.ansible.com/list#/users/15516)
  - [https://hub.docker.com/u/marcelocorreia/](https://hub.docker.com/u/marcelocorreia/)
  - Any issues, pull-request are welcome

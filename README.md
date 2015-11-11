# nomad-install

Installs [Hasicorp's Nomad] (https://nomadproject.io)



## Role Variables
```yml

---
nomad_app:
  name: nomad
  version: 0.1.2
  arch: linux_amd64
  file_owner: vagrant
  file_group: vagrant

install:
  dir : /usr/local/bin
  download_location: https://dl.bintray.com/mitchellh/nomad
  file_list:
    - nomad

```


Example Playbook
----------------
```yml


- hosts: local
  sudo: true
  gather_facts: true

  roles:
    - { role: marcelocorreia.nomad-install }

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

NodeJS
========

Installs NodeJS.

Installation
--------------

`ansible-galaxy install palkan.nodejs`

Role Variables
--------------

`defaults/main.yml`

| Name                        | Default Value |  Description    |
|-----------------------------|---------------|-----------------|
| node_version                 | 0.12.5        | Version to install |
| node_prefix                  | "node-v{{ node_version }}" | |
| node_tarball                 | "{{ node_prefix }}.tar.gz" | |
| node_path                    | "/usr/local" | |
| node_tmp_path                | "/tmp" | |

Example Playbook
-------------------------
```yml
  - hosts: servers
    roles:
       - palkan.nodejs
```

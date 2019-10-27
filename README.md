# ansible-role-nginx

Role for install & config specific version of Nginx from the yum repository (CentOS 7)

## Example Playbook
```
---
- name: install nginx & php
  hosts:
    - vagrant-be
  become: true
  vars:
    nginx_version: "lastest"
    nginx_worker_processes: "auto"
    nginx_worker_rlimit_nofile: "2048"
    nginx_worker_connections: "2048"
  roles:
    - role: nginx
```

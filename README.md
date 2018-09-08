Traefik (in Docker) role for Ansible
====

#### Dependencies

- Assumes Docker and Docker Compose are installed on the host

#### Usage

Create a playbook (`traefik.yml`) from this role:

```
---
- name: Install and configure Traefik reverse-proxy
  hosts: <your host group or individual host>
  roles:
    - role: roles/traefik
      traefik_docker_domain: "mydomain.org"
      traefik_acme_email: "user@mydomain.org"
      traefik_dashboard_basicauth_users: ["user:$apr1$somehash"]
```

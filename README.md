[![Build Status](https://github.com/rezizter/ansible-loki/actions/workflows/ci.yml/badge.svg)](https://github.com/rezizter/ansible-loki/actions/workflows/ci.yml)

# ansible-loki

An Ansible role to install Grafana Loki and Promtail.

## Requirements

For the standard (from binary) install of loki/promtail:

- `unzip` on the hosts

For the dockerized promtail:

- Python: `docker==4.3.1`
- `docker-cli`

## Role Variables

See `defaults/main.yml` to customize this role.

## Dependencies

_None._

## Example Playbook

This role is driven by inventory groups:

```yaml
all:
  hosts:
    monitoring.host.example.org:
  children:
    loki:
      monitoring.host.example.org:
    promtail:
      monitoring.host.example.org:
```

And the playbook:

```yaml
- hosts: all
  roles:
    - role: hostwithquantum.loki
```

## License

BSD-2-Clause

## Author Information

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

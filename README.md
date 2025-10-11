# Ansible Role: Wireshark

[![CI](https://github.com/pluggero/ansible-role-wireshark/actions/workflows/ci.yml/badge.svg)](https://github.com/pluggero/ansible-role-wireshark/actions/workflows/ci.yml) [![Ansible Galaxy downloads](https://img.shields.io/ansible/role/d/pluggero/wireshark?label=Galaxy%20downloads&logo=ansible&color=%23096598)](https://galaxy.ansible.com/ui/standalone/roles/pluggero/wireshark)

An Ansible Role that installs a basic configuration of wireshark.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

```yaml
wireshark_version: "x.x"
```

The version of wireshark to install can be defined in the variable `wireshark_version`.

```yaml
wireshark_install_method: "dynamic"
```

The method used to install wireshark can be defined in the variable `wireshark_install_method`.
The following methods are available:

- `source`: Installs wireshark from source
- `package`: Installs wireshark from the package manager of the distribution
  - **NOTE**: This method installs the latest version available in the package manager and not the version defined in `wireshark_version`.
- `dynamic`: Installs wireshark from package manager if available in the correct version, otherwise installs from source


## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - pluggero.wireshark
```

## License

MIT / BSD

## Author Information

This role was created in 2025 by Robin Plugge.

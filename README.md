# generate_ssh_keys

An [Ansible](https://www.ansible.com) role that generates SSH keys for the Ansible [control node](https://docs.ansible.com/ansible/latest/network/getting_started/basic_concepts.html#control-node).

- RSA
- DSA
- ECDSA
- ED25519

<p align="center">
<a href="https://app.codacy.com/gh/dgibbs64/ansible-role-generate_ssh_keys"><img src="https://img.shields.io/codacy/grade/1a892d499efd4dabb73beffa8d64ed01?logo=codacy&style=flat-square" alt="Codacy grade"></a>
<a href="https://github.com/dgibbs64/ansible-role-generate_ssh_keys/actions/workflows/molecule.yml"><img alt="GitHub Workflow Status" src="https://img.shields.io/github/workflow/status/dgibbs64/ansible-role-generate_ssh_keys/Ansible%20Molecule?label=molecule&logo=ansible&style=flat-square"></a>
<a href="https://galaxy.ansible.com/dgibbs64/generate_ssh_keys"><img alt="Ansible Quality Score" src="https://img.shields.io/ansible/quality/60208?logo=ansible&style=flat-square"></a>
<a href="https://galaxy.ansible.com/dgibbs64/generate_ssh_keys"><img alt="Ansible Role" src="https://img.shields.io/ansible/role/d/60208?color=EE0000&logo=ansible&style=flat-square"></a>
<a href="https://galaxy.ansible.com/dgibbs64/generate_ssh_keys"><img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/dgibbs64/ansible-role-generate_ssh_keys?color=EE0000&label=release&logo=ansible&style=flat-square"></a>
<a href="https://github.com/dgibbs64/ansible-role-first_contact/blob/main/LICENSE.md"><img src="https://img.shields.io/github/license/gameservermanagers/ansible-role-generate_ssh_keys?style=flat-square" alt="MIT License"></a>
</p>

## Requirements

None.

## Role Variables

The default values for the variables are set in `defaults/main.yml`:

```yaml
key_directory: "~/.ssh"
key_rsa: "id_rsa"
key_dsa: id_dsa
key_ecdsa: "id_ecdsa"
key_ed25519: "id_ed25519"
ssh_key_comment: "ansible-ssh-key"
```

## Dependencies

None.

## Example Playbook

This example is taken from `molecule/default/converge.yml` and is tested on each push, pull request and release.

```
---
- name: converge
  hosts: all
  gather_facts: false

  roles:
    - role: dgibbs64.generate_ssh_keys
```

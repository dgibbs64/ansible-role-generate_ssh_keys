# generate_ssh_keys

An [Ansible](https://www.ansible.com) role that generates SSH keys for the Ansible [control node](https://docs.ansible.com/ansible/latest/network/getting_started/basic_concepts.html#control-node).

- RSA
- DSA
- ECDSA
- ED25519

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

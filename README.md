# SatNOGS Ansible

Ansible scripts for SatNOGS infra

## Requirements

1. Ansible (duh..)
2. GPG
3. Running gpg-agent

## Usage

Assuming you have sudo access and `hosts.gpg` is decrypted:

```
ansible-playbook main.yml
```

**Note:** Some sensitive files like `hosts` and `private.yml` are
    encrypted with [ansible-vault][]. `vault-passwd.txt.gpg` is
    automatically decrypted during playbook run. That saves us time
    from running `--vault-password-file vault-passwd.txt` each time.
    The password is decrypted on the fly without the need to decrypt
    to plain text file.

[ansible-vault]: http://docs.ansible.com/playbooks_vault.html

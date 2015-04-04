# SatNOGS Ansible

Ansible scripts for SatNOGS infra

## Usage

Assuming you have sudo access and `hosts.gpg` and `vault-passwd.txt.gpg` are
decrypted:

`ansible-playbook main.yml --vault-password-file vault-passwd.txt`

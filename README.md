# SatNOGS Ansible

Ansible scripts for SatNOGS infra

## Requirements

1. Ansible (duh..)
2. GPG
3. Running gpg-agent

## Usage

Assuming you have sudo access run the whole thing:

```
ansible-playbook -v main.yml --extra-vars "db_tag=x.x net_tag=x.x"
```

when asked for your gpg key, provide it and the plays will run.

The secret variables encryption rationale is described in
<https://github.com/axilleas/ansible-bootstrap>.

## License

&copy; 2014-2015 [Libre Space Foundation](http://librespacefoundation.org).

Licensed under the [Creative Commons Attribution-ShareAlike 3.0 License](LICENSE).

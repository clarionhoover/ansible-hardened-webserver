# ansible-hardened-webserver
## Purpose
The purpose of this repository is to contain an ansible playbook with a collection of roles to configure a secure hardened baseline to allow you to deploy a web application knowing the basic security principles have been applied.

## How to Use
To use this playbook, just run the below commands:
```
1. ansible-galaxy install -r requirements.yml -p roles/ --force
2. Add a random string to the .vault_pass file
3. Fill out needed variables in vars/all_vars.yml and vars/vault.yml
4. ansible-vault encrypt vars/vault.yml
5. ansible-playbook playbook.yml -e @vars/all_vars.yml -e @vars/vault.yml -i hosts/production
```
<p><b><span style="color:red">NOTE:</span></b> This playbook requires no password for sudo, and requiretty disabled for your ansible user. Or you can disable pipelining in the ansible.cfg file</p>

## Contributing
TODO

## Contributors
TODO

## License
License is the MIT License located in [LICENSE.md](LICENSE.md)

Ansible Role: Docker
====================

Role to install Docker Engine and Docker Compose

Requirements
------------

N/A

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml) for the details

Dependencies
------------

N/A

Example Playbook
----------------

Create `my_playbook.yml` with the following contents:
```yaml
- hosts: localhost
  remote_user: root
  roles:
    - docker
```

And then run - this will install Docker and Docker Compose to the `localhost` host:
```bash
ansible-playbook my_playbook.yml
```

Docker or Docker Compose installation can be switched on/off using tags. Example (only Docker-Compose will be installed):
```bash
ansible-playbook -t docker-compose my_playbook.yml
```

Contribution
------------

Use `test.sh` script to prepare test environment and run [Molecule](https://molecule.readthedocs.io/en/latest/) tests for the role

Author Information
------------------

[vi7](https://github.com/vi7)

This is an [Ansible](http://www.ansible.com/home) role for an
installation of [Flower](http://flower.readthedocs.io/en/latest/).

# What it Does

Installs the `flower` Python module (using the `pip` module), defines
a `flower` service, and sets up logging, configuration of that
service.

# Usage

Use the role in a playbook like this:

```yaml
- hosts: all
  roles:
    - flower
```

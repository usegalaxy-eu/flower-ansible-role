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

This role installs `celery`, however if you want to use your own celery, you can set the `{{ flower_venv_dir }}` variable.
For using apps with `flower`, it is important to set the `{{ flower_app_dir }}` variable to the app directory, which will be also the service working directory. The `{{ flower_app_name }}` is only the module name.  
When using this role for Galaxy servers, please set both:

- `{{ flower_app_dir }}`
- `{{ flower_python_path }}` (can be relative to app dir)

It is recommended to store `{{ flower_ui_users }}` and broker url/api vars in `secret_group_vars`.

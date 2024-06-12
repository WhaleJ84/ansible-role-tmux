tmux
=========

Installs and configures tmux for the user.

Requirements
------------

To include this role in your `requirements.yml` file, add the following list item:

```yaml
---
roles:
  - names: whalej84.tmux
    src: https://github.com/WhaleJ84/ansible-role-tmux.git
    scm: git
```

Example Playbook
----------------

This example playbook shows how I would use this role, with custom variables to suit my needs.

```yaml
- hosts: localhost

  roles:
     - role: whalej84.tmux
       tags: [ tmux ]
```

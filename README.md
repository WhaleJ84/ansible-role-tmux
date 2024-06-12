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

Role Variables
--------------

| Name | Type | Description | Default |
| ---- | ---- | ----------- | ------- |
| tmux\_config\_dir | string | A path to where the tmux config files should be located | "$HOME" |
| tmux\_config | string | A path to where the tmux config should be located | "{{ tmux\_config\_dir }}/tmux.config" |

Example Playbook
----------------

This example playbook shows how I would use this role, with custom variables to suit my needs.

```yaml
- hosts: localhost

  roles:
     - role: whalej84.tmux
       vars:
         tmux_config_dir: "{{ ansible_user_dir }}/.config/tmux"
       tags: [ tmux ]
```

gnome shell
==========

Installs gnome-shell and adds module to manage gnome-shell extensions

Requirements
------------

This role requires Ansible 2.0 or higher.

Role Variables
--------------

| Name                   | Default                            | Description                              |
|------------------------|------------------------------------|------------------------------------------|
| gnome_extension_path   | /usr/share/gnome-shell/extensions/ | path to extensions                       |
| gnome_extension_owner  | root                               | owner of the extension                   |
| gnome_shell_extensions | []                                 | extension id's which should be installed |

Dependencies
------------

Example Playbook
----------------

Install gnome-shell and the extensions:
- https://extensions.gnome.org/extension/442/drop-down-terminal/
- https://extensions.gnome.org/extension/1005/focus-my-window/

```
- hosts: all
  roles:
   - { role: ansible-gnome_shell, gnome_extension_path: /home/edi/.local/share/gnome-shell/extensions/, gnome_extension_owner: edi, gnome_shell_extensions: [442, 1005] }
```

License
-------

BSD

Author Information
------------------

Eduard Angold


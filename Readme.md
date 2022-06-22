Ansible Role Powershell
=========

Installs Powershell on Debian/Ubuntu servers. 
Releases: https://github.com/PowerShell/PowerShell/releases/tag/v7.2.2

Role Variables
--------------

```
# Version of 'powershell to install, defaults to latest version
powershell_version: ""

# Toggling this will uninstall from the server
uninstall: false
```

Example Playbooks
----------------

Minimal:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.powershell
```

Specific Version:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.powershell
      vars:
        powershell_version: "7.2.2"
```

Uninstall:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.powershell
      vars:
        uninstall: true
```
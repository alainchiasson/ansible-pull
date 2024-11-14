Role Name
=========

This role is designed to manage various system services and packages using Ansible. It includes tasks for configuring network settings, installing and managing packages, and setting up services. 

Requirements
------------

- Ansible 2.1 or higher
- The following Ansible collections:
  - `community.general`
  - `ansible.posix`

Role Variables
--------------

The following variables can be set in `defaults/main.yml`, `vars/main.yml`, or passed in as parameters:

- `hostname`: The hostname to configure (default: `localhost.localdomain`)
- `timezone`: The timezone to configure (default: `Etc/UTC`)

Dependencies
------------

This role has no dependencies on other roles.

Example Playbook
----------------

Here is an example of how to use this role:

```yaml
- hosts: all
  become: true
  roles:
    - role: base
      hostname: "services.home.chiasson.org"
      timezone: "Etc/UTC"
```

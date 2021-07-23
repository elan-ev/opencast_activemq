Ansible: Opencast ActiveMQ Role
===============================

This Ansible role installs and prepares ActiveMQ for Opencast.
ActiveMQ will be configured with no authentication but will accept local connections only.
This will work if it is installed on Opencast's admin node.

Role Variables
--------------

- `opencast_repository_identifiers`
    - List of repository identifiers to temporarily activate for integration
	 - Will usually be provided by the `opencast_repository` role
- `opencast_version_major`
    - Opencast major version to get the configuration for

Dependencies
------------

This role requires `elan.opencast_repository`.


Example Playbook
----------------

Example of how to configure and use the role:

```yaml
- hosts: servers
  become: true
  roles:
    - role: elan.opencast_activemq
      opencast_version_major: 10
```

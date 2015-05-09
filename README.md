HostsFile
=========

This role manages the /etc/hosts file. By default the role wont make any changes if the variable hosts_file not defined.

Role Variables
--------------

This role takes only one variable "hosts_file" to define hosts entries for ipv4 and ipv6.


Example Playbook
----------------

Playbook example of include:

```
- hosts: servers
  roles:
   - HostsFile
```

The variable can be defined in two places host_vars or group_vars. Recommended to define this variable only in group_vars on the cluster level.

Example of variable defenition:

group_vars/web-servers-atlanta-dc1.yml
```
	---
	hosts_file:
	 ipv4:
	  - "10.0.0.2	api.internal.example.org"
	  - "10.0.0.3	search.internal.example.org	search"
	 ipv6:
	  - "fe80::200:f8ff:fe21:67cf api.internal.example.org"
```


Author Information
------------------

Tal Lannder

Tal@Pjili.com

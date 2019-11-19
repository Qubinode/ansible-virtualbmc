Role Name
=========

- installs virtual-bmc service and registers all defined KVM VMs in the service
- generate instackfile that can be imported in undercloud

Role Variables
--------------

var_name | default | desc
------- | ------- | -------
manage_firewall: | True | if the role should manage firewalld (flushes iptables, and enables firewalld and adds necessary ports)
instack_user: | stack | username that should have access to generated instack file
instackfile_path: | /home/{{instack_user}} | directory where to generate instackfile

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        manage_firewall: True
        instack_user: stack
        instackfile_path: "/home/{{instack_user}}"
      roles:
         - role: virtual-bmc

License
-------

BSD

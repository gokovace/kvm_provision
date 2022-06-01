Role Name
=========

Deploy KVM virtual machine using ansible
VM will have one NAT-ed interface for going out and one private to communicate with other VMs

Requirements
------------

1) If SSH key is not generated make it with ssh-keygen
2) Edit defaults/main.yaml to suit your needs

Role uses community.libvirt.virt module so install it prior to running a playbook with:
$ ansible-galaxy collection install community.libvirt

https://docs.ansible.com/ansible/latest/collections/community/libvirt/virt_module.html

Role Variables
--------------

Set up following variables:
vm_type : ubuntu/centos
vm_name: master1
vm_vcpus: 2
vm_ram_mb: 4096
ssh_key: /home/gkovacevic/.ssh/localvm_key.pub

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

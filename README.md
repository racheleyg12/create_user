create_user
=========

Create a user and upload an ssh public key for remote authenication

Requirements
------------

No specific required Ansible
Needs a default ssh public key or a specific key needs to be called out in a variable.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

#Define the user you would like to create
user_name: default
#Define the user state present or absent
user_state: present
#Define the path to the ssh public key
ssh_key: ~/.ssh/id_rsa.pub

Dependencies
------------

None

Example Playbook
----------------

---
- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         user_state: present
         ssh_key: ~/.ssh/cloud_key.pub

License
-------

MIT
BSD

Author Information
------------------

info@kumul.us

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

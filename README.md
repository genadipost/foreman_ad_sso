foreman_ad_sso
=========

Ansible role to configure Active Directory (AD) as an external authentication source for Foreman server.

Requirements
------------

The role uses [```expect```](http://docs.ansible.com/ansible/latest/expect_module.html) module.

- python >= 2.6 
- pexpect >= 3.3 
- ansible > 2.0 

Role Variables
--------------

| Name    | Description    | Required    | Default    | Values | Examples |
|:--|:--|:-:|:-:|:-:|:--|
| ad_user | Active directory user used to add the machine to domain | Yes | - | - | Administrator |
| ad_user_password | Active directory user password | Yes | - | - | Pa$$word |
| domain | Active directory domain name | Yes | - | - | test.local |

Dependencies
------------

* `genadipost.epel_repositories`
* `genadipost.puppet_repositories`
* `genadipost.foreman_repositories`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: foreman
      roles:
         - { role: genadipost.foreman_ad_sso, ad_user: Administrator, ad_user_password: Pa$$word, domain: test.local }

License
-------

BSD

Author Information
------------------

genadipost@gmail.com

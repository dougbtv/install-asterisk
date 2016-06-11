install-asterisk
=========

This is an ansible role for installing Asterisk, it tracks Asterisk 13 certified branch.

Requirements
------------

This role is intended to install Asterisk from source on CentOS / Fedora. It will focus on the Certified branch initially. CentOS is required now, 6 & 7 supported. Likely works on CentOS 5.5.

Role Variables
--------------

(none yet)

Example Playbook
----------------

Here's the vanilla way to use it, to install Asterisk:

    - hosts: servers
      roles:
         - { role: install-asterisk }

But, if you'd like to configure the user asterisk runs as you can do:

    - hosts: servers
      roles:
         - { role: install-asterisk, configure_user: true, asterisk_user: "asterisk", asterisk_group: "asterisk" }

The `asterisk_user` and `asterisk_group` are optional, and default the "asterisk". If you don't want to configure the user, just omit the variable entirely.


Steps to run the installation:

1) git clone https://github.com/dougbtv/install-asterisk.git
2) copy one of the examples above into asterisk.yml
3) define hosts in a file named hosts
4) command line: ansible-playbook -i hosts asterisk.yml -u root

License
-------

MIT

Author Information
------------------

Doug Smith
dougbtv.com
@dougbtv

install-asterisk
=========

This is an ansible role for installing Asterisk.

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
         - { role: dougbtv.install-asterisk }

But, if you'd like to configure the user asterisk runs as you can do:

    - hosts: servers
      roles:
         - { role: dougbtv.install-asterisk, configure_user: true, asterisk_user: "asterisk", asterisk_group: "asterisk" }

The `asterisk_user` and `asterisk_group` are optional, and default the "asterisk". If you don't want to configure the user, just omit the variable entirely.

License
-------

MIT

Author Information
------------------

Doug Smith
dougbtv.com
@dougbtv

install-asterisk
=========

This is an ansible role for installing Asterisk, it tracks Asterisk 13 certified branch.

Requirements
------------

This role is intended to install Asterisk from source on CentOS / Fedora. It will focus on the Certified branch initially. CentOS is required now, 6 & 7 supported. Likely works on CentOS 5.5.

Role Variables
--------------

(none yet)

Install via ansible-galaxy
--------------------------

Use ansible galaxy to download this role with:

    ansible-galaxy install dougbtv.install-asterisk

Example Playbook
----------------

Here's the vanilla way to use it, after installing via ansible-galaxy, to install Asterisk:

    - hosts: servers
      roles:
         - { role: dougbtv.install-asterisk }

But, if you'd like to configure the user asterisk runs as you can do:

    - hosts: servers
      roles:
         - { role: dougbtv.install-asterisk, configure_user: true, asterisk_user: "asterisk", asterisk_group: "asterisk" }

The `asterisk_user` and `asterisk_group` are optional, and default the "asterisk". If you don't want to configure the user, just omit the variable entirely.


Use via git clone
-----------------

Alternatively, you can clone this repository and use the example `test.yml` playbook to test it out, and base your usage on that.

1. Clone the repository `git clone https://github.com/dougbtv/install-asterisk.git`
2. Change the defined hosts in the `test.inventory` file.
3. Execute the: `ansible-playbook -i test.inventory test.yml`

License
-------

MIT

Author Information
------------------

Doug Smith
dougbtv.com
@dougbtv

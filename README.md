openstack-dev
=============

Configure a VM with some of the dependencies needed for OpenStack
development and prepare it to have the source repositories checked
out.

Creates a directory (openstack_dev_repos_dir) containing a script to
check out all OpenStack repositories.

Checks out a copy of the global requirements repository, including the
tool for building wheels for all of the known dependencies to speed
unit test environment building (it does not run the script).

Requirements
------------

None

Role Variables
--------------

* openstack_dev_repos_dir

  Base directory where source repositories will be checked
  out. Defaults to $HOME/repos.

Dependencies
------------

- dhellmann.python-dev
- dhellmann.devpi

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: dhellmann.openstack-dev, openstack_dev_repos_dir: "/mnt/repos" }

License
-------

BSD

Author Information
------------------

Doug Hellmann
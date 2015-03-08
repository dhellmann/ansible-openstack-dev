openstack-dev
=============

Configure a VM with some of the dependencies needed for OpenStack
development and prepare it to have the source repositories checked
out.

Requirements
------------

None

Role Variables
--------------

* openstack_dev_repos_dir

  Base directory where source repositories will be checked
  out. Defaults to $HOME/repos. A script, update.sh, is dropped into
  this directory to invoke the script in the oslo-incubator for
  cloning all of the repositories under the openstack namespace under
  git.openstack.org.

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
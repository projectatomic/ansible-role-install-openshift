install-openshift
=================

Installs OpenShift v3 from various sources. Right now there is only one source,
RPMs from COPR.

This role is part of
[ansible-osbs](https://github.com/projectatomic/ansible-osbs/) playbook for
deploying OpenShift build service. Please refer to that github repository for
[documentation](https://github.com/projectatomic/ansible-osbs/blob/master/README.md)
and [issue tracker](https://github.com/projectatomic/ansible-osbs/issues).

Role Variables
--------------

You need to specify which method of installation you want to use. Valid options
are `copr` (default).

    install_openshift_method: copr

You must specify particular version that should be installed from the COPR.
Can be in either `version` or `version-release` format.

    install_openshift_copr_version: 1.0.5

Example Playbook
----------------

    - hosts: builders
      roles:
         - role: install-openshift
           install_openshift_method: copr

License
-------

BSD

Author Information
------------------

Martin Milata &lt;mmilata@redhat.com&gt;

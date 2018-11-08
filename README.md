Ansible Role: P4 CLI
=========

[![Build Status](https://travis-ci.org/mattandes/ansible-role-p4cli.svg?branch=master)](https://travis-ci.org/mattandes/ansible-role-p4cli)

This role will install the Perforce (P4/Helix) CLI client on a Linux system from the Perforce repositories.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    p4cli_package: helix-cli

Name of the P4 client package to be installed

    p4cli_package_state: present

Determines state of the package.

    p4cli_rpm_key: https://package.perforce.com/perforce.pubkey

The location of the public key for the Perforce yum repositories.

    p4cli_yum_repo_url: "http://package.perforce.com/yum/rhel/{{ ansible_distribution_major_version }}/x86_64"

The URL for the Perforce yum repositories.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: mattandes.p4cli

License
-------

MIT

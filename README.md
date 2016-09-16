# Ansible Role: SVN

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-svn.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-svn)

Installs [Apache SVN](https://subversion.apache.org/) (Subversion) on any RHEL/CentOS or Debian/Ubuntu Linux system.

## Requirements

The `svnserve` service, which allows access to repositories via the `svn://` protocol runs on port 3690 by default, so please make sure that port is open on your firewall.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    svn_repository_home: /var/svn

The SVN repository directory that will be served by `svnserve` through Apache.

    svn_create_test_repo: true

Whether to create a example respository 'testrepo', which will be available at `http://[hostname]/svn/testrepo`.

## Dependencies

  - geerlingguy.apache

## Example Playbook

    - hosts: servers
      roles:
        - geerlingguy.svn

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](http://www.jeffgeerling.com/), author of [Ansible for DevOps](https://www.ansiblefordevops.com/).

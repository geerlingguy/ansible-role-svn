# Ansible Role: SVN

Installs SVN on any RHEL/CentOS Linux system.

## Requirements

The `svnserve` service, which allows access to repositories via the `svn://` protocol runs on port 3690 by default, so please make sure that port is open on your firewall.

## Role Variables

Available variables are listed below, along with default values (see `vars/main.yml`):

    svn_create_test_repo: true

Whether to create a example respository 'testrepo', which will be available at `http://[hostname]/svn/testrepo`.

## Dependencies

  - geerlingguy.repo-epel
  - geerlingguy.apache

## Example Playbook

    - hosts: servers
      vars_files:
        - vars/main.yml
      roles:
        - { role: geerlingguy.svn }

*Inside `vars/main.yml`*:

    TODO

## License

MIT / BSD

## Author Information

This role was created in 2014 by Jeff Geerling (@geerlingguy), author of Ansible for DevOps. You can find out more about the book at http://ansiblefordevops.com/, and learn about the author at http://jeffgeerling.com/.

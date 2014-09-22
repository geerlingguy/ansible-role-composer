# Ansible Role: Composer

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-composer.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-composer)

Installs Composer, the PHP Dependency Manager, on any Linux or UNIX system.

## Requirements

`curl` and `php` (version 5.3+) should be installed and working.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    composer_path: /usr/local/bin/composer

The path where composer will be installed and available to your system. Should be in your user's `$PATH` so you can run commands simply with `composer` instead of the full path.

    composer_keep_updated: false

Set this to `true` to update Composer to the latest release every time the playbook is run.

## Dependencies

  - geerlingguy.php (Installs PHP).

## Example Playbook

    - hosts: servers
      roles:
        - { role: geerlingguy.composer }

After the playbook runs, `composer` will be placed in `/usr/local/bin/composer` (this location is configurable), and will be accessible via normal system accounts.

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).

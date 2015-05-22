# Vagrant LAMP based on Ubuntu Precise

Provisioned using Ansible.

Disclamer:
If you need a LAMP stack with the latest Ubuntu and packages, basically don't use this.
I created it as I needed Ubuntu Precise and PHP 5.3.

## What's inside?

  - Ubuntu Precise64
  - Aapche 2.2.x
  - PHP 5.3.x (+ php5-gd)
  - MySQL 5.5.x
  - Composer
  - Drush (configurable)

## Dependencies (VirtualBox, Vagrant, Ansible)

  1. VirtualBox
  2. Vagrant
  3. Ansible

Project tested on MAC only.

## How to use it?

Your website's index needs to be into data/site

Then copy the default config file:
$ cp default-config.yml config.yml

Start the VM:
$ vagrant up

## Variables available

  - vagrant_hostname
  - locale
  - language
  - timezone
  - site_root_path
  - db_name
  - db_user
  - db_password
  - php_max_execution_time
  - php_memory_limit
  - drush_version

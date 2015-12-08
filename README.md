# Vagrant LAMP based on Ubuntu Precise

Provisioned using Ansible.

Disclamer:
- This is a setup for development only, do not use in production.
- If you need a LAMP stack with the latest Ubuntu and packages, basically don't use this.
- I created it as I needed Ubuntu Precise and PHP 5.3.

## What's inside?

  - Ubuntu Precise64
  - Aapche 2.2.x
  - PHP 5.3.x (+ php5-gd + php5-curl + php5-xdebug*)
  - MySQL 5.5.x
  - Composer
  - Drush (configurable)

* Remove the commented lines on xdebug's configuration file to activate it.

## Dependencies

  1. VirtualBox
  2. Vagrant
  3. Ansible

Project tested on MAC.

## How to use it?

Your website's index needs to be into a subfolder: data/site/www

You can also configure the path using the variable site_root_path. See bellow Variables available.

Copy the default config file: $ cp default-config.yml config.yml

Start the VM: $ vagrant up

## Variables available

Some variables availables to be configured into your config.yml:
  - vagrant_hostname
  - vagrant_ip
  - vm_ram
  - locale
  - language
  - timezone
  - site_root_path
  - mysql_root_password
  - db_name
  - db_user
  - db_password
  - php_max_execution_time
  - php_memory_limit
  - drush_version

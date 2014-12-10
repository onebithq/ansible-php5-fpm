Role Name
=========

This role installs and configures the php5-fpm.

Requirements
------------

This role requires Ansible 1.4 or higher and platform requirements are listed
in the metadata file.

Role Variables
--------------

A description of the settable variables for this role    
    - php_conf_pm: process control method (dynamic or static)    
    - php_conf_max_children : maximum number of child processes to be alive    
    - php_conf_start_servers : the number of children created on startup
    - php_conf_min_spare_servers : the minimum number of children in 'idle'    
    - php_conf_max_spare_servers : the maximum number of children in 'idle'    

Dependencies
------------

[]

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: onebitlibs.php5-fpm, 
         	 php_conf_max_children: 2, 
         	 php_conf_pm: static,
         	 ubuntu_pkg: [ php5-common, php5-curl ] }

License
-------

BSD

Author Information
------------------

Author : lagilaper / onebitlibs (www.onebitmedia.com)

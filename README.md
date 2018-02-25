Atlassian Confluence
=========

Ansible role for installing Atlassian Confluence. Tested platforms are:
* Debian 8
* Ubuntu 16

Requirements
------------

Debian 8 (jessie)
Ubuntu 16 (xenial)

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

| Parameter | Required | Default | Choices | Comments |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| default_download_directory | yes | /tmp | | Sets directory where files will be downloaded |
| confluence_version  | yes | 6.7.1 | | Sets Atlassian Confluence version for installing  |
| atlassian_user_name | yes  | atlassian | | Sets Confluence system user to run with /sbin/nologin |
| confluence_directory | yes  | confluence | | Sets Confluence directory name. Example /home/[:atlassian_user_name]/[:confluence_directory] |
| confluence_home_directory | yes  | confluence-home | | Sets Confluence directory for all file. Example /home/[:atlassian_user_name]/[:confluence_home_directory] |
| java_home_directory | yes  | /usr/lib/jvm | | Sets path to JAVA_HOME |
| java_mysql_connector_version | yes  | 5.1.45 | | Sets version for MySQL java connector |





Dependencies
------------

    dependencies:
     - role: antonchernik.oracle-jdk

Example 
----------------
    ---
    - hosts: all
      roles:
         - { role: antonchernik.atlassian-confluence }

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2017 by [Anton Chernik](https://github.com/antonchernik).

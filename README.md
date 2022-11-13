Plexamp Headless
=========

This role installs plexamp-headless along with the needed pre-requirements.

Requirements
------------

None

Role Variables
--------------
Available variables are listed below, along with default values (see defaults/main.yml):

|Name|Default Value|Description|
|--|--|--|
| plexamp_user | plexamp | Sets the user (and group) that plexamp will be installed and run as|
|plexamp_uid | 1001 | Used for the uid of the above user|
|plexamp_archive | https://plexamp.plex.tv/headless | URL to download plexamp from|
|plexamp_stream | version | The stream to check headless version from|

Dependencies
------------

None.

Example Playbook
----------------

Here is a basic setup:

    - hosts: servers
      roles:
         - plexamp-headless

License
-------

GPL v2+

Author Information
------------------

This role was created by [Edward McLain](https://github.com/zonywhoop/).

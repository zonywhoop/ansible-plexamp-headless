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
| plexamp_user | plexamp | Sets the user (and group) that plexamp will be installed and run as |
| plexamp_uid | 1001 | Used for the uid of the above user |
| plexamp_archive | https://plexamp.plex.tv/headless | URL to download plexamp from |
| plexamp_stream | version | The stream to check headless version from |

Dependencies
------------

* Your machine needs to have a supported Alsa sound installed and working in linux.
* Plexamp Headless supports alsa, jack, and pulse-audio audio engines
* You need a Plex server to connect to and a plex account

Example Playbook
----------------

Here is a basic setup:

    - hosts: servers
      roles:
         - plexamp-headless


**This only needs to be run on first install**

On first install you will need to run plexamp and claim your player. You can do this by running the command below as **root** and following the prompts.
```
cd /home/{plexamp_user}/plexamp
sudo -u {plexamp_user} node js/index.js
```

License
-------

GPL v2+

Author Information
------------------

This role was created by [Edward McLain](https://github.com/zonywhoop/).

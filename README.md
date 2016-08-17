nvidia-blob-install
=========
Crudge install script for nvidia driver. It is desined for CUDA/servers application and avoid messing up with xserver. (It you have one - do not use this role).

It uses nvidia installer in blob form. If your distribution have better way to install actual drivers, use it (for debian it is 'nvidia-driver' package).


Requirements
------------

apt, internet access, nvidia hardware. Should be run as root or with 'become: yes'

Role Variables
--------------

nvidia\_dirver\_version. Default is to current version, '367.35'.

Dependencies
------------

none

Example Playbook
----------------


- hosts: all
  become: yes
  vars:
   - nvidia_dirver_version: 370.23
  roles:
   - nvidia-blob-install

License
-------

BSD

Author Information
------------------

(c) George Shuklin, 2016

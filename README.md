Ansible role: packer [![Build Status](https://travis-ci.org/craneworks/ansible-packer.png)](https://travis-ci.org/craneworks/ansible-packer)
=========

An Ansible role that install Hashicorps Packer

Requirements
------------

On the host must `unzip` being installed.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

	packer_version: 0.8.6

The version which should be installed.

	packer_sha256sum: 2f1ca794e51de831ace30792ab0886aca516bf6b407f6027e816ba7ca79703b5

The sha256sum of the downloaded zip file.

  packer_base_url: https://releases.hashicorp.com/packer

Base URL from Hashicorps mirror.

	packer_arch: amd64

Architecture which should be used.

	packer_download_cache: /tmp/packer.zip

Destination where the zip file should be cached.

	packer_path: /opt/packer

Info file where the version is being stored

Dependencies
------------

None

Example Playbook
----------------

    - hosts: buildservers
      roles:
         - { role: craneworks.packer, packer_version: 0.8.0, packer_sha256sum: 74b21580a7734fd6a025cfbba5ec60b85a61cd7c99ffe87904c4c013c801e6d2 }

License
-------

CC-BY - https://creativecommons.org/licenses/by/3.0/

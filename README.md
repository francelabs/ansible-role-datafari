# Ansible Role : Datafari 


Installs Datafari Community Edition 5.5+ into Debian 11 or Ubuntu 22

## Requirements

This role uses the community.general ansible Collection.
Java 11 only must be installed on the server.
We use alvistack.openjdk role in order to do so.

This role is currently tested for Datafari 5.5+.

### Remote host
This role relies on a set of packages that are mandatory for Datafari. All the packages are listed into files/apt.

## Role Variables


Available variables are listed below, with default values, (see [defaults/main.yml](defaults/main.yml)):
Datafari version to install. Minimum supported is 5.5
  datafari_version: 5.5

Password for Datafari, MCF and Postgresql
  password: admin

Directory into Datafari is downloaded 
  datafari_download_dir: /tmp

## Dependencies


## Example Playbook


    - hosts: all
      become: true
      vars:
        openjdk_release: "11"
      roles:
        - alvistack.openjdk
        - francelabs.datafari

## License

Apache 2

## Author Information

This role was created in August 2023 by Olivier Tavard - France Labs.

## Changelog

Changelog can be found here [CHANGELOG.md](CHANGELOG.md)
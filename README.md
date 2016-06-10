# NodeJS

[![License](https://img.shields.io/badge/license-New%20BSD-blue.svg?style=flat)](https://raw.githubusercontent.com/ansiblebit/nodejs/master/LICENSE)
[![Build Status](https://travis-ci.org/ansiblebit/nodejs.svg?branch=master)](https://travis-ci.org/ansiblebit/nodejs)

[![Platform](http://img.shields.io/badge/platform-debian-a80030.svg?style=flat)](#)
[![Platform](http://img.shields.io/badge/platform-ubuntu-dd4814.svg?style=flat)](#)

[![Project Stats](https://www.openhub.net/p/ansiblebit-nodejs/widgets/project_thin_badge.gif)](https://www.openhub.net/p/ansiblebit-nodejs/)

[Ansible][ansible] role to setup [NodeJS][nodejs].


## Tests

| Family | Distribution | Version | Test Status |
|:-:|:-:|:-:|:-:|
| Debian | Debian  | Jessie  | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |
| Debian | Debian  | Wheezy  | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |
| Debian | Ubuntu  | Yakkety | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |
| Debian | Ubuntu  | Xenial  | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |
| Debian | Ubuntu  | Trusty  | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |
| Debian | Ubuntu  | Precise | [![x86_64](http://img.shields.io/badge/x86_64-passed-006400.svg?style=flat)](#) |

## Requirements

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here.
For instance, if the role uses the EC2 module,
it may be a good idea to mention in this section that the boto package is required.

- ansible >= 1.9


## Role Variables

- *nodejs_apt_dependencies*: the APT dependencies needed to run this role.
- *nodejs_dir_src*: directory where to store the [NodeJS][nodejs] source.
- *nodejs_path*: the directory where to install [NodeJS][nodejs].
- *nodejs_prefix*: the filename prefix of the [NodeJS][nodejs] tarball.
- *nodejs_tarball*: the filename for the [NodeJS][nodejs] tarball.
- *nodejs_version*: [NodeJS][nodejs] version to be installed.


## Dependencies

None.


## Playbooks

  - hosts: servers
    roles:
       - palkan.nodejs


## Tags

- **configuration**: configuration tasks.
- **debug**: task to debug role variables.
- **installation**: installation tasks.
- **validation**: task to validate role variables.


## Test

To run the tests you will need to install:

- [tox](https://tox.readthedocs.org/)
- [vagrant](https://www.vagrantup.com/)

To run all tests against all pre-defined OS/distributions * ansible versions:

```
$ tox
```

To run tests for `trusty64`:

```
$ cd tests
$ bash test_idempotence.sh --box trusty64.vagrant.dev
# log file will be stores under tests/log
```

To perform debugging on a specific environment:

```
$ cd tests
$ vagrant up trusty64.vagrant.dev

# to provision using the test.yml playbook (as many time as you need)
$ vagrant provision trusty64.vagrant.dev

# to access the Vagrant box
$ vagrant ssh trusty64.vagrant.dev
```


## Links

- [NodeJS][nodejs]
- [palkan/nodejs][palkan/nodejs]


## License

[BSD][bsd]


## Author Information

- [palkan][palkan]
- [steenzout][steenzout]

[ansible]:      https://www.ansible.com         "Ansible"
[bsd]:          https://github.com/ansiblebit/nodejs/blob/master/LICENSE "BSD license"
[nodejs]:       https://nodejs.org/             "NodeJS"
[palkan]:       https://github.com/palkan/      "Vladimir Dementyev"
[palkan/nodejs]: https://github.com/palkan-ansible/nodejs "Palkan's NodeJS Ansible role"
[steenzout]:    http://github.com/steenzout/    "Pedro Salgado"

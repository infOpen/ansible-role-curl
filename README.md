# curl

[![Build Status](https://img.shields.io/travis/infOpen/ansible-role-curl/master.svg?label=travis_master)](https://travis-ci.org/infOpen/ansible-role-curl)
[![Build Status](https://img.shields.io/travis/infOpen/ansible-role-curl/develop.svg?label=travis_develop)](https://travis-ci.org/infOpen/ansible-role-curl)
[![Updates](https://pyup.io/repos/github/infOpen/ansible-role-curl/shield.svg)](https://pyup.io/repos/github/infOpen/ansible-role-curl/)
[![Python 3](https://pyup.io/repos/github/infOpen/ansible-role-curl/python-3-shield.svg)](https://pyup.io/repos/github/infOpen/ansible-role-curl/)
[![Ansible Role](https://img.shields.io/ansible/role/25442.svg)](https://galaxy.ansible.com/infOpen/curl/)

Install curl package.

## Requirements

This role requires Ansible 2.2 or higher,
and platform requirements are listed in the metadata file.

## Testing

This role use [Molecule](https://github.com/metacloud/molecule/) to run tests.

Local and Travis tests run tests on Docker by default.
See molecule documentation to use other backend.

Currently, tests are done on:
- Debian Jessie
- Ubuntu Trusty
- Ubuntu Xenial

and use:
- Ansible 2.2.x
- Ansible 2.3.x
- Ansible 2.4.x
- Ansible 2.5.x

### Running tests

#### Using Docker driver

```
$ tox
```

## Role Variables

### Default role variables

``` yaml
# Installation
curl_packages: "{{ _curl_packages }}"
curl_repository_cache_valid_time: 3600
curl_repository_update_cache: True
```

### Debian OS family specific vars

``` yaml
_curl_packages:
  - name: 'curl'
```

## Dependencies

None

## Example Playbook

``` yaml
- hosts: servers
  roles:
    - { role: infOpen.curl }
```

## License

MIT

## Author Information

Alexandre Chaussier (for Infopen company)
- http://www.infopen.pro
- a.chaussier [at] infopen.pro

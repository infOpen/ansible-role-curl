# curl

[![CI](https://github.com/infOpen/ansible-role-curl/workflows/CI/badge.svg)](https://github.com/infOpen/ansible-role-curl/actions)
[![Mergify Status][mergify-status]][mergify]
[![Updates](https://pyup.io/repos/github/infOpen/ansible-role-curl/shield.svg)](https://pyup.io/repos/github/infOpen/ansible-role-curl/)
[![Python 3](https://pyup.io/repos/github/infOpen/ansible-role-curl/python-3-shield.svg)](https://pyup.io/repos/github/infOpen/ansible-role-curl/)
[![Ansible Role](https://img.shields.io/ansible/role/25442.svg)](https://galaxy.ansible.com/infOpen/curl/)

Install curl package.

## Requirements

This role requires Ansible 2.8 or higher,
and platform requirements are listed in the metadata file.

## Testing

This role use [Molecule](https://github.com/ansible-community/molecule) to run tests.

Local and Github Actions tests run tests on Docker by default.
See molecule documentation to use other backend.

Currently, tests are done on:
- CentOS 7
- CentOS 8
- Debian Buster
- Debian Stretch
- Ubuntu Bionic
- Ubuntu Focal

and use:
- Ansible 2.8.x
- Ansible 2.9.x

### Running tests

#### Using Docker driver

```
$ tox
```

You can also configure molecule options and molecule command using environment variables:
* `MOLECULE_OPTIONS` Default: "--debug"
* `MOLECULE_COMMAND` Default: "test"

```
$ MOLECULE_OPTIONS='' MOLECULE_COMMAND=converge tox
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
- https://www.infopen.pro
- a.chaussier [at] infopen.pro

[mergify]: https://mergify.io
[mergify-status]: https://img.shields.io/endpoint.svg?url=https://gh.mergify.io/badges/infOpen/ansible-role-curl&style=flat

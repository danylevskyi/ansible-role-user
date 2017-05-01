# Ansible Role: User

[![Build Status](https://travis-ci.org/danylevskyi/ansible-role-user.svg?branch=master)](https://travis-ci.org/danylevskyi/ansible-role-user)

Create users, configure their ssh private keys and set authorized keys for created users.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    user_users: []

A list of users to create.

## Dependencies

None.

## Example Playbook

    - hosts: servers

      vars:
        user_users:
          - name: example_user
            ssh_private_key_path: "../app_keys/id_rsa"
            authorized_key_path: false

      roles:
         - { role: danylevskyi.user }

Provided example will create `example_user` with `id_rsa` ssh private key.

## TODO

  - Add tests.

## License

BSD / MIT

## Author Information

This role was created in 2017 by [Dmytro Danylevskyi](http://dmytro.danylevskyi.com/).

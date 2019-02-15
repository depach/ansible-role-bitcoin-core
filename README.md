# Ansible Role: litecoin Core

An Ansible role that compiles and installs litecoind, litecoin-cli and litecoin-tx (e.g. headless) on Debian like systems.

Forked From https://github.com/lifeofguenter/ansible-role-bitcoin-core

## Requirements

none

## Role Variables

- `litecoin_version: 0.17.1`

- `litecoin_user: litecoin`

- `litecoin_home: "/home/{{ litecoin_user }}"`

- `litecoin_conf_datadir: "{{ litecoin_home }}"`

- `litecoin_conf_pid: /run/litecoind/litecoind.pid`

See https://litecoin.info/index.php/Litecoin.conf#litecoin.conf_Configuration_File for more options (prefix them with `litecoin_conf_`)

## Dependencies

none

## Example Playbook

```
- hosts: miner
  roles:
    - { role: depach.litecoin-core }
```

## Thank you

- Gunter Grodotzki ([lifeofguenter](https://github.com/lifeofguenter/)) for [ansible-role-bitcoin-core](https://github.com/lifeofguenter/ansible-role-bitcoin-core)
- Cédric Félizard ([infertux](https://github.com/infertux)) for [munin-bitcoin](https://github.com/infertux/munin-bitcoin)

## License

[MIT](LICENSE)

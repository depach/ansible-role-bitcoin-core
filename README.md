# Ansible Role: Bitcoin Core

An Ansible role that compiles and installs bitcoind, bitcoin-cli and bitcoin-tx (e.g. headless) on Debian like systems.

Forked From https://github.com/lifeofguenter/ansible-role-bitcoin-core

## Requirements

none

## Role Variables

- `bitcoin_version: 0.17.1`

- `bitcoin_user: bitcoin`

- `bitcoin_home: "/home/{{ bitcoin_user }}"`

- `bitcoin_conf_datadir: "{{ bitcoin_home }}"`

- `bitcoin_conf_pid: /run/bitcoind/bitcoind.pid`

See https://en.bitcoin.it/wiki/Running_Bitcoin#Bitcoin.conf_Configuration_File for more options (prefix them with `bitcoin_conf_`)

## Dependencies

none

## Example Playbook

```
- hosts: miner
  roles:
    - { role: lifeofguenter.bitcoin-core }
```

## Thank you

- Gunter Grodotzki ([lifeofguenter](https://github.com/lifeofguenter/) for [ansible-role-bitcoin-core](https://github.com/lifeofguenter/ansible-role-bitcoin-core)
- Cédric Félizard ([infertux](https://github.com/infertux)) for [munin-bitcoin](https://github.com/infertux/munin-bitcoin)

## License

[MIT](LICENSE)

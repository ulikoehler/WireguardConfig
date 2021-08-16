# GuardMyWire
Generate wireguard configs for Linux and MikroTik devices

## Installation

Install the required dependencies using
```sh
pip3 install -r requirements.txt
```
and just run the script in place

## Howto use

First, you need to create your JSON config files. See the [examples](https://github.com/ulikoehler/GuardMyWire/tree/master/examples), e.g. [Site2Site.json](https://github.com/ulikoehler/GuardMyWire/blob/master/examples/Site2Site.json).

Then, run
```sh
python3 guardmywire.py my-config.json
```

This will generate a `my-config` directory containing:
* A `config` directory containing `wg-quick` config files (the "normal" WireGuard config files - also for the Windows client
* A `keys` directory containing private, public and pre-shared keys for all the peers
* A `mikrotik` directory containing files with MikroTik terminal commands to setup the interface. RouterOS v7 required (v6 does not support Wireguard!)
* [WIP] A `mobile` directory with mobile QR codes

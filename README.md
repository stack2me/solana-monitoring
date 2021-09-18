# solana-monitoring

Roles of Ansible for monitor solana node.

## System requirements

- Ubuntu 18 or newest
- Python 3.x

## Roles:

- **prometheus-node-exporter** install prometheus exporter
  - exporter for hardware and OS metrics exposed
  - Install nginx for close entry points of monitoring systems
- **solana-monitor** install script to add custom solana node metrics

## Installation

- Pull repository
- Add your host to `hosts` file
- Change nginx user/password for basic_auth in `vars/variables.yml`
- Run ansible: `ansible-playbook solana.yaml -i hosts.yaml --ask-become-pass -v --ask-pass`
- Install grafana [Solana Validator Dashboard](https://grafana.com/grafana/dashboards/14625)

## Example Dashboard based on prometheus-node-exporter

![Alt text](images/image.png?raw=true "Solana dashboard")

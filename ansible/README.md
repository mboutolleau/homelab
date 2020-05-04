# Ansible playbooks and roles to manage a personal infrastructure

## Inventory

The Ansible inventory is static and written in the `hosts` file (not published on this repo).

## Playbooks

- `update-system.yml` : safely upgrades all packages of a Debian based host (uses the `apt` module)
# Ansible playbooks and roles to manage a personal infrastructure

## Inventory

The Ansible inventory is static and written in the `hosts` file (not published on this repo) or can be specified with the `-i/--inventory` option of `ansible-playbook`.

## Playbooks

### `deploy-alacritty-terminfo`

Deploy the [Alacritty](https://github.com/alacritty/alacritty) [terminfo](https://www.man7.org/linux/man-pages/man5/terminfo.5.html) to a Linux host.

### `deploy-caddy.yml`

Deploy the [Caddy web server](https://caddyserver.com/) v2 to a Debian based host (uses a `.deb` package and the `apt` module) along with a dummy configuration file and a sample `systemd` unit. See [../software/caddy](../software/caddy).

### `update-system.yml`

Safely upgrades all packages of a Debian based host (uses the `apt` module). Does not automatically restart a host if needed after the upgrade. 

## Usage

    ansible-playbook --inventory "<host>," <playbook>.yml

If you need to specicy a become password (with `sudo` for example), add the `-K/--ask-become-pass` option.
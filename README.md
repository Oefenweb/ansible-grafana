## grafana

[![Build Status](https://travis-ci.org/Oefenweb/ansible-grafana.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-grafana)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-grafana-blue.svg)](https://galaxy.ansible.com/Oefenweb/grafana)

Set up (the latest version of) Grafana in Debian-like systems.

#### Requirements

None

#### Variables

* `grafana_install`: [default: `[]`]: Additional packages to install

* `grafana_grafana_user`: [default: `grafana`]: User to run daemon as
* `grafana_grafana_group`: [default: `grafana`]: Group to run daemon as
* `grafana_grafana_home`: [default: `/usr/share/grafana`]: Home directory
* `grafana_log_dir`: [default: `/var/log/grafana`]: L:g directory
* `grafana_data_dir`: [default: `/var/lib/grafana`]: Data directory
* `grafana_max_open_files`: [default: `10000`]: Maximum number of open files
* `grafana_conf_dir`: [default: `/etc/grafana`]: Configuration directory
* `grafana_conf_file`: [default: `/etc/grafana/grafana.ini`]: Configuration file
* `grafana_restart_on_upgrade`: [default: `true`]: Whether or not to restart on upgrade
* `grafana_plugins_dir`: [default: `/var/lib/grafana/plugins`]: Plugins directory
* `grafana_pid_file_dir`: [default: `/var/run/grafana`]: PID file (`run`) directory

* `grafana_etc_default`: [see: `defaults/main.yml`]: Content (lines) of `/etc/default/grafana-server`

* `grafana_etc_grafana_grafana_ini`: [default: `[]`]: Content (lines) of `/etc/grafana/grafana.ini` ([see](https://github.com/grafana/grafana/blob/master/conf/sample.ini))

## Dependencies

None

#### Example(s)

##### Simple

```yaml
---
- hosts: all
  roles:
    - grafana
```

##### Custon configuration

```yaml
---
- hosts: all
  roles:
    - grafana
  vars:
    grafana_etc_grafana_grafana_ini:
      - |
        [server]
        http_addr = 127.0.0.1
```

#### License

MIT

#### Author Information

* Mark van Driel
* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-grafana/issues)!

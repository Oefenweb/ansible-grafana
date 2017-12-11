## grafana

[![Build Status](https://travis-ci.org/Oefenweb/ansible-grafana.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-grafana) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-grafana-blue.svg)](https://galaxy.ansible.com/Oefenweb/grafana)

Set up (the latest version of) Grafana in Debian-like systems.

#### Requirements

None

#### Variables

* `grafana_install`: [default: `[]`]: Additional packages to install

* `grafana_grafana_user`: [default: `grafana`]: 
* `grafana_grafana_group`: [default: `grafana`]: 
* `grafana_grafana_home`: [default: `/usr/share/grafana`]: 
* `grafana_log_dir`: [default: `/var/log/grafana`]: 
* `grafana_data_dir`: [default: `/var/lib/grafana`]: 
* `grafana_max_open_files`: [default: `10000`]: 
* `grafana_conf_dir`: [default: `/etc/grafana`]: 
* `grafana_conf_file`: [default: `/etc/grafana/grafana.ini`]: 
* `grafana_restart_on_upgrade`: [default: `true`]: 
* `grafana_plugins_dir`: [default: `/var/lib/grafana/plugins`]: 
* `grafana_pid_file_dir`: [default: `/var/run/grafana`]: 

* `grafana_etc_default`: [see: `defaults/main.yml`]: 

* `grafana_etc_grafana_grafana_ini`: [default: `[]`]: 

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - grafana
```

#### License

MIT

#### Author Information

* Mark van Driel
* Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-grafana/issues)!

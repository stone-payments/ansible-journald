stone-payments.journald
============
Ansible role to enforce configuration of a journald log system

# Quickstart
Just have a systemd-journald instance installed, set up the variables defined
in defaults/main.yml as you wish and include the role.
```
- name: configure journald
  hosts: all
  roles: stone-payments.journald
```
# Configs
The defaults provided here are the same of a EL7.4 default distribution.
```
journald_storage_option: "auto"
journald_compress_option: "yes"
journald_seal_option: "yes"
journald_splitmode: "uid"
journald_sync_interval: "5m"
journald_rate_limit_interval: "30s"
journald_rate_limit_burst: "1000"
journald_system_max_use: ""
journald_system_keep_free: ""
journald_max_file_size: ""
journald_runtime_max_use: ""
journald_runtime_keep_free: ""
journald_runtime_max_file_size: ""
journald_max_retention_sec: ""
journald_max_file_sec: "1month"
journald_forward_to_syslog: "yes"
journald_forward_to_kmsg: "no"
journald_forward_to_console: "no"
journald_forward_to_wall: "yes"
journald_tty_path: "/dev/console"
journald_max_level_store: "debug"
journald_max_level_syslog: "debug"
journald_max_level_kmsg: "notice"
journald_max_level_console: "info"
journald_max_level_wall: "emerg"

```

# License
This role is distributed under the MIT License.

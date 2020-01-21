# Ansible role 'ntp'

An Ansible role for setting up NTP servers and clients.
There are vars files for several distros, but since galaxy-publishing only the one listed in the meta has been tested. Further testing on other distros is needed.


## Requirements

## Role Variables
| Variable                      | Default                          | Comments (type)  |
| :---                          | :---                             | :---             |
| is_ntp_server                 | False                            | Node is a server, ntpd only (True/False)|
| ntp_servers | see default/main.yml | list of servers to poll |
| ntp_allow | not defined | An IP subnet allowed to poll node, used with chrony instad if `is_ntp_server` (e.g. 10.0.0.1/24) |
| ntp_stratum | not defined | string for defining local stratum level (e.g `local stratum 10`)|
| ntp_timezone | Europe/Stockholm | timezone to use |
## Dependencies

## Example Playbook
```Yaml
- hosts: foo
  roles:
    - { role: oscpe262.ntp }
  vars:
    ntp_servers:
      - 10.0.0.10
      - 10.0.0.11
```

## Testing

## License

MIT

## Contributors

Issues, feature requests, ideas, suggestions, etc. are appreciated and can be posted in the Issues section. Pull requests are also very welcome. Please create a topic branch for your proposed changes, it's the easiest way to merge back into the project.

- [Oscar Petersson](https://github.com/oscpe262/) (Maintainer)

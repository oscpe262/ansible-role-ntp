# Ansible role 'ntp'

An Ansible role for setting up NTP servers and clients. The role defaults to clients syncronizing to 192.168.0.102. Adjust according to your needs.

## Requirements
Minimum, either of:
- Arch Linux
- CentOS 7
- Linux Mint 18
- Ubuntu 16.10

Might work on other distributions as well, but these are tested.

## Role Variables
| Variable                      | Default                          | Comments (type)  |
| :---                          | :---                             | :---             |
| ntp_enabled                   | yes                              | Enables service (Yes/No)|
| ntp_state                     | restarted                          | Starts service (started/restarted/stopped) |
| ntp_server                    | False                            | Node is a server (True/False)|
| ntp_srv_ip  | 192.168.0.102 | Server IP |

## Dependencies

## Example Playbook
```Yaml
- hosts: foo
  roles:
    - { role: ntp, ntp_server: True, ntp_srv_ip: '127.0.0.1' }
```

## Testing

## License

BSD

## Contributors

Issues, feature requests, ideas, suggestions, etc. are appreciated and can be posted in the Issues section. Pull requests are also very welcome. Please create a topic branch for your proposed changes, it's the easiest way to merge back into the project.

- [Oscar Petersson](https://github.com/oscpe262/) (Maintainer)

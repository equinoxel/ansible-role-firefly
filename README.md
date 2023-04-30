# Firefly Ansible role

This role installs Firefly via Docker compose.

## Requirements

None

## Role Variables

All variables are listed below (see also `defaults/main.yml`).

| Name | Description | Default value |
| --- | --- | --- |
|`firefly_image: firefly`| Docker image to be used | latest |
|`firefly_http_port_app`| Firefly application port|  30000 |
|`firefly_timezone`| Timezone |  "Europe/Brussels" |
| Map coordinates | |
|`firefly_map_lat`| Latitude |  51.983333 |
|`firefly_map_long`| Longitude |  5.916667 |
|`firefly_map_zoom`| Zoom |  6 |
| Application | |
|`firefly_app_name`| Application name |  "Firefly III" |
|`firefly_app_key`| Unique application key. Must be 32 chars long |  "12345678901234567890123456789012" |
|`firefly_owner_email`| Owner email |  "user@domain.com" |
| Database | |
|`firefly_db_password`| Database password (note: MySQL backend) |  "changeme" |
| Cron | |
|`firefly_static_cron_token`| Cron token for firefly |  "12345678901234567890123456789012" |
| Firefly paths | |
|`firefly_root_path`| Default base for configuration |  /var/local |
|`firefly_config_path`| Location of the configuration files|  "{{ firefly_root_path }}/conf/firefly" |

## Dependencies

You need a machine with docker and docker-compose installed.

## Example Playbook

```yml
- hosts: servers
  roles:
      - 'laurivan.firefly'
```

## License

This project is licensed under the [MIT](https://opensource.org/licenses/MIT) license - see the [LICENSE](LICENSE) file for details.

![MIT License](https://img.shields.io/badge/license-MIT%20License-brightgreen)

## Author Information

This role was created in 2023 by [Laur Ivan](https://www.laurivan.com).

## Built With

![Ansible](https://img.shields.io/badge/ansible-5.2.0-green.svg)
![Molecule](https://img.shields.io/badge/molecule-3.4.0-green.svg)
![Goss](https://img.shields.io/badge/goss-0.3.16-green.svg)

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

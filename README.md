# Ansible Role: certbot-rfc2136
[![Gitlab pipeline status (self-hosted)](https://img.shields.io/gitlab/pipeline/dubzland/ansible-role-certbot?gitlab_url=https%3A%2F%2Fgit.dubzland.net)](https://git.dubzland.net/dubzland/ansible-role-certbot/pipelines)

Handles installing [Certbot](https://certbot.eff.org) for managing [Let's Encrypt](https://letsencrypt.org) certificates.

## Requirements

Ansible version 2.0 or higher

## Role Variables

Available variables are listed below, along with their default values (see `defaults/main.yml` for more info):

### dubzland_certbot_configuration_directory

```yaml
dubzland_certbot_configuration_directory: /etc/certbot
```

Directory to contain certbot certificate configuration files.

### dubzland_certbot_certs

```yaml
dubzland_certbot_certs: []
```

List of certificates to configure for retrieval.

### dubzland_certbot_retrieve_certs

```yaml
dubzland_certbot_retrieve_certs: True
```

Whether or not to actually retrieve certificates.

## Dependencies

None

## Example Playbook

```yaml
- hosts: web-servers
  roles:
    - role: dubzland.certbot-rfc2136
```

## License

MIT

## Author

* [Josh Williams](https://codingprime.com)

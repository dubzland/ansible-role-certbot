# Ansible Role: certbot-rfc2136
[![Gitlab pipeline status (self-hosted)](https://img.shields.io/gitlab/pipeline/dubzland/ansible-role-certbot-rfc2136?gitlab_url=https%3A%2F%2Fgit.dubzland.net)](https://git.dubzland.net/dubzland/ansible-role-certbot-rfc2136/pipelines)

Handles installing [Certbot](https://certbot.eff.org) for managing [Let's Encrypt](https://letsencrypt.org) certificates.

## Requirements

Ansible version 2.0 or higher

## Role Variables

Available variables are listed below, along with their default values (see `defaults/main.yml` for more info):

### dubzland_certbot_rfc2136_configuration_directory

```yaml
dubzland_certbot_rfc2136_configuration_directory: /etc/certbot
```

Directory to contain certbot certificate configuration files.

### dubzland_certbot_rfc2136_certs

```yaml
dubzland_certbot_rfc2136_certs: []
```

List of certificates to configure for retrieval.

### dubzland_certbot_rfc2136_dry_run

```yaml
dubzland_certbot_rfc2136_dry_run: False
```

When `True`, certificates will be obtained from Let's Encrypt's staging
environment.

### dubzland_certbot_rfc2136_deploy_hook

```yaml
dubzland_certbot_rfc2136_deploy_hook:
```

When supplied, should be a command to run after a certificate is successfully
renewed. ex: `dubzland_certbot_rfc_2136_deploy_hook: systemctl reload nginx`.

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

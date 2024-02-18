A simple role to install bind9 on Debian.

This role assumes that you have existing bind9 configuration files which you
likely have checked into some revision control system. These have the options,
the local configuration, and a directory of zone files.

- named.conf.options
- named.conf.local
- configs/
  - example.com.db
  - example.org.db

The named.conf.local file would reference the files in the configs/ directory.

# Examples
## Playbook
Here's an example of a playbook to install bind9 on the local machine. It
does not require you have SSH running.

```yaml
- hosts: localhost
  connection: local
  become: true
  roles:
    - role: hax0rbana_adam.bind9
```

This playbook expects that your bind9 configuration files are in the working
directory.

# Official repo location
All activity takes place on the official GitLab instance:
[https://gitlab.hax0rbana.org/public-repos/ansible/bind9](https://gitlab.hax0rbana.org/public-repos/ansible/bind9)

Any other hosting providers, such as GitHub.com and GitLab.com, are just mirrors
and we do not monitor the issue trackers over there.

# Support
## Matrix channel
You can also join our Matrix channel: #ansible:hax0rbana.org

This is a good place to ask questions or make requests without having to sign
up for another account.

## Fediverse
If you prefer the Fediverse to Matrix, you can find the primary author of this
package at: `@adam@hax0rbana.social`

# Contributing
See [contributor guidelines](CONTRIBUTING.md).

# License
This project is licensed under MIT License. See [LICENSE](LICENSE) for more details.

<!-- DOCSIBLE START -->

# 📃 Role overview

## waal70.virtualbox

Description: This role installs Oracle's VirtualBox

### Defaults

These are static variables with lower priority

#### File: defaults/main.yml

| Var | Type | Value |
| -------------- | -------------- | ------------- |
| [vbox_apt_key_url](defaults/main.yml#L3) | str | `https://www.virtualbox.org/download/oracle_vbox_2016.asc` |
| [vbox_repo_url](defaults/main.yml#L4) | str | `https://download.virtualbox.org/virtualbox/debian` |
| [vbox_apt_suite](defaults/main.yml#L7) | str | `trixie` |
| [vbox_apt_components](defaults/main.yml#L8) | str | `contrib` |
| [vbox_apt_arch](defaults/main.yml#L10) | str | `{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64' }}` |
| [vbox_install_version](defaults/main.yml#L12) | str | `7.2` |

### Tasks

#### File: tasks/main.yml

| Name | Module | Has Conditions |
| ---- | ------ | -------------- |
| Add the VirtualBox apt repository | ansible.builtin.deb822_repository | False |
| Install required VirtualBox packages | ansible.builtin.apt | False |

## Author Information

waal70 (Andre)

### License

GPL

#### Minimum Ansible Version

2.1

#### Platforms

- **Debian**: ['bookworm']

#### Dependencies

No dependencies specified.
<!-- DOCSIBLE END -->

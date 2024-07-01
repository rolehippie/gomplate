# gomplate

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/gomplate)
[![General Workflow](https://github.com/rolehippie/gomplate/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/gomplate/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/gomplate/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/gomplate/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/gomplate/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/gomplate/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/gomplate)](https://github.com/rolehippie/gomplate/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.gomplate-blue)](https://galaxy.ansible.com/rolehippie/gomplate)

Ansible role to install gomplate template processor.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [gomplate_arch](#gomplate_arch)
  - [gomplate_download](#gomplate_download)
  - [gomplate_version](#gomplate_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### gomplate_arch

Architecture of the static binary

#### Default value

```YAML
gomplate_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64' }}"
```

### gomplate_download

URL to the archive of the release to install

#### Default value

```YAML
gomplate_download: https://github.com/hairyhenderson/gomplate/releases/download/v{{
  gomplate_version }}/gomplate_linux-{{ gomplate_arch }}
```

### gomplate_version

Version of the release to install

#### Default value

```YAML
gomplate_version: 4.0.1
```

## Discovered Tags

**_gomplate_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)

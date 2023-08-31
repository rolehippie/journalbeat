# journalbeat

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/journalbeat)
[![General Workflow](https://github.com/rolehippie/journalbeat/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/journalbeat/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/journalbeat/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/journalbeat/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/journalbeat/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/journalbeat/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/journalbeat)](https://github.com/rolehippie/journalbeat/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.journalbeat-blue)](https://galaxy.ansible.com/rolehippie/journalbeat)

Ansible role to install and configure journalbeat.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [journalbeat_console_enabled](#journalbeat_console_enabled)
  - [journalbeat_default_inputs](#journalbeat_default_inputs)
  - [journalbeat_default_processors](#journalbeat_default_processors)
  - [journalbeat_group_inputs](#journalbeat_group_inputs)
  - [journalbeat_group_processors](#journalbeat_group_processors)
  - [journalbeat_host_inputs](#journalbeat_host_inputs)
  - [journalbeat_host_processors](#journalbeat_host_processors)
  - [journalbeat_keyring](#journalbeat_keyring)
  - [journalbeat_logging_level](#journalbeat_logging_level)
  - [journalbeat_logging_selectors](#journalbeat_logging_selectors)
  - [journalbeat_logging_to_files](#journalbeat_logging_to_files)
  - [journalbeat_logstash_enabled](#journalbeat_logstash_enabled)
  - [journalbeat_logstash_hosts](#journalbeat_logstash_hosts)
  - [journalbeat_major_version](#journalbeat_major_version)
  - [journalbeat_name](#journalbeat_name)
  - [journalbeat_service_enabled](#journalbeat_service_enabled)
  - [journalbeat_tags](#journalbeat_tags)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### journalbeat_console_enabled

#### Default value

```YAML
journalbeat_console_enabled: false
```

### journalbeat_default_inputs

List of default inputs, gets directly transformed to yaml

#### Default value

```YAML
journalbeat_default_inputs:
  - paths: []
    seek: cursor
```

### journalbeat_default_processors

List of default processors, gets directly transformed to yaml

#### Default value

```YAML
journalbeat_default_processors:
  - add_host_metadata:
  - add_cloud_metadata:
  - add_docker_metadata:
```

### journalbeat_group_inputs

List of group inputs, merged with journalbeat_default_inputs

#### Default value

```YAML
journalbeat_group_inputs: []
```

### journalbeat_group_processors

List of group processors, merged with journalbeat_default_processors

#### Default value

```YAML
journalbeat_group_processors: []
```

### journalbeat_host_inputs

List of host inputs, merged with journalbeat_default_inputs

#### Default value

```YAML
journalbeat_host_inputs: []
```

### journalbeat_host_processors

List of host processors, merged with journalbeat_default_processors

#### Default value

```YAML
journalbeat_host_processors: []
```

### journalbeat_keyring

Path for the repository keyring

#### Default value

```YAML
journalbeat_keyring: /usr/share/keyrings/elastic-archive-keyring.gpg
```

### journalbeat_logging_level

Define logging level

#### Default value

```YAML
journalbeat_logging_level: warning
```

### journalbeat_logging_selectors

Define logging selectors, like beat, publish, service

#### Default value

```YAML
journalbeat_logging_selectors: []
```

### journalbeat_logging_to_files

Log to files, keep journal clean

#### Default value

```YAML
journalbeat_logging_to_files: true
```

### journalbeat_logstash_enabled

#### Default value

```YAML
journalbeat_logstash_enabled: true
```

### journalbeat_logstash_hosts

#### Default value

```YAML
journalbeat_logstash_hosts: []
```

### journalbeat_major_version

Major version to install, used for the APT repository

#### Default value

```YAML
journalbeat_major_version: 7
```

### journalbeat_name

Name of the shipper within the output

#### Default value

```YAML
journalbeat_name: '{{ ansible_hostname }}'
```

### journalbeat_service_enabled

Enable the console output

### journalbeat_tags

List of tags to assign for the shipper

#### Default value

```YAML
journalbeat_tags: []
```

## Discovered Tags

**_journalbeat_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)

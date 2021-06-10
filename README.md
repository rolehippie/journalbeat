# journalbeat

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/journalbeat) [![Testing Build](https://github.com/rolehippie/journalbeat/workflows/testing/badge.svg)](https://github.com/rolehippie/journalbeat/actions?query=workflow%3Atesting) [![Readme Build](https://github.com/rolehippie/journalbeat/workflows/readme/badge.svg)](https://github.com/rolehippie/journalbeat/actions?query=workflow%3Areadme) [![Galaxy Build](https://github.com/rolehippie/journalbeat/workflows/galaxy/badge.svg)](https://github.com/rolehippie/journalbeat/actions?query=workflow%3Agalaxy) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/journalbeat)](https://github.com/rolehippie/journalbeat/blob/master/LICENSE) 

Ansible role to install and configure journalbeat. 

## Sponsor 

[![Proact Deutschland GmbH](https://proact.eu/wp-content/uploads/2020/03/proact-logo.png)](https://proact.eu) 

Building and improving this Ansible role have been sponsored by my employer **Proact Deutschland GmbH**.

## Table of content

* [Default Variables](#default-variables)
  * [journalbeat_console_enabled](#journalbeat_console_enabled)
  * [journalbeat_default_inputs](#journalbeat_default_inputs)
  * [journalbeat_default_processors](#journalbeat_default_processors)
  * [journalbeat_group_inputs](#journalbeat_group_inputs)
  * [journalbeat_group_processors](#journalbeat_group_processors)
  * [journalbeat_host_inputs](#journalbeat_host_inputs)
  * [journalbeat_host_processors](#journalbeat_host_processors)
  * [journalbeat_logging_level](#journalbeat_logging_level)
  * [journalbeat_logging_selectors](#journalbeat_logging_selectors)
  * [journalbeat_logging_to_files](#journalbeat_logging_to_files)
  * [journalbeat_logstash_enabled](#journalbeat_logstash_enabled)
  * [journalbeat_logstash_hosts](#journalbeat_logstash_hosts)
  * [journalbeat_major_version](#journalbeat_major_version)
  * [journalbeat_name](#journalbeat_name)
  * [journalbeat_service_enabled](#journalbeat_service_enabled)
  * [journalbeat_tags](#journalbeat_tags)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

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

## Dependencies

* None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)

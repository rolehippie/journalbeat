# journalbeat

[![Build Status](https://cloud.drone.io/api/badges/rolehippie/journalbeat/status.svg)](https://cloud.drone.io/rolehippie/journalbeat)

Ansible role to configure journalbeat

## Table of content

* [Default Variables](#default-variables)
  * [journalbeat_service_enabled](#journalbeat_service_enabled)
  * [journalbeat_service_state](#journalbeat_service_state)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

## Default Variables

### journalbeat_service_enabled

Switch the service into enabled state

#### Default value

```YAML
journalbeat_service_enabled: false
```

### journalbeat_service_state

State for the service definition

#### Default value

```YAML
journalbeat_service_state: stopped
```

## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)

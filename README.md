![](assets/header.png)

Welcome to TheHive Project's Docker Templates repository.

It's hosting docker configurations for TheHive, Cortex and 3rd party tools integrations.

# What's in it?

This repository aims to be a location where TheHive and Cortex users can find and share docker compose configuration files for

- TheHive
- Cortex
- MISP
- Reverse Proxies
- OAuth Providers
- Workflow and automation tools
- Feeders

## Common configurations

This section should describe the common configuration that can be commonly used in diverse docker-compose templates relying on TheHive and/or Cortex
### TODO

Add documentation on possible application config for TheHive and Cortex images

- How to configure TheHive
  - `application.conf` file
  - `logback.xml` file
- How to configure Cortex
  - dockerized neurons
  - local neurons
  - permissions
  - `application.conf` file
  - `logback.xml` file

## Available configuration

- [TheHive 3 + Cortex 3](./docker/thehive3-cortex3-es7)
- [Cortex 3 with dockerized neurons](./docker/cortex3-dockerized-neurons)

## TODO

The list bellow includes the docker-compose configurations to be done:

- [ ] TheHive 3 + Elasticsearch
- [ ] TheHive 4 + BerkleyDB
- [ ] TheHive 4 + Cassandra
- [ ] Cortex 3 + dockerized neurons
- [ ] Cortex 3 + local neurons
- [ ] Add reverse proxy
  - [ ] Nginx ?
  - [ ] Traefik ?
- [ ] Add oauth providers
  - [ ] keycloak ?
  - [ ] Fusionauth ?


# Contributing
Please see our [Code of conduct](code_of_conduct.md). We welcome your contributions. Please feel free to fork the code, play with it, make some patches and send us pull requests via [issues](https://github.com/TheHive-Project/TheHive/issues).
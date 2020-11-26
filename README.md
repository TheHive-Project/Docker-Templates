<div>
  <p align="center">
    <img src="assets/header.png" width="700"/>  
  </p>
</div>
<div>
  <p align="center">
    <a href="https://chat.thehive-project.org" target"_blank">
      <img src="https://img.shields.io/discord/779945042039144498" alt="Discord">
    </a>
    <a href="./LICENSE" target"_blank">
      <img src="https://img.shields.io/github/license/TheHive-Project/Docker-Templates" alt="License">
    </a>
    <a href="./LICENSE" target"_blank">
      <img src="https://img.shields.io/docker/pulls/thehiveproject/thehive?color=%23f8c218&label=Thehive%20docker%20pulls" alt="License">
    </a>
    <a href="./LICENSE" target"_blank">
      <img src="https://img.shields.io/docker/pulls/thehiveproject/cortex?color=%2347b7b7&label=Cortex%20docker%20pulls" alt="License">
    </a>
    
  </p>
</div>

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

## Common configuration

This section describes the possible configuration options for the major components

### How to configure Elasticsearch

```
TODO
```

### How to configure Cassandra

```
TODO
```
### How to configure TheHive

- How to configure TheHive
  - volumes
    - `application.conf` file
    - `logback.xml` file
    - local file storge 
  - command configs

```
TODO
```
### How to configure Cortex
- How to configure Cortex
  - dockerized neurons
  - local neurons
  - permissions
  - volumes
    - `application.conf` file
    - `logback.xml` file

```
TODO
```

## Available templates

### Basic templates
- [TheHive 4 + Cassandra](./docker/thehive4-cassandra)
- [TheHive 3.5 + Cortex 3.1](./docker/thehive35-cortex31-es7)
- [Cortex 3 with dockerized neurons](./docker/cortex3-dockerized-neurons)
### Custom templates

#### TheHive 4.x

- [TheHive 4 + Cortex 3 + MISP 2.4.134 + Shuffle 0.8.0](./docker/thehive4-cortex3-misp-shuffle) by [@garanews](https://github.com/garanews)
- [TheHive 4 + Cassandra + Traefik + Route53](./docker/thehive4-cassandra3-traefik-route53) by [@aacgood](https://github.com/aacgood) 

#### Thehive 3.5 (Elasticsearc 7)

- [TheHive 3.5 + Cortex 3.1 + ES 7 + Traefik + Route53](./docker/thehive35-cortex3-es7-traefik-route53) by [@aacgood](https://github.com/aacgood) 
- [TheHive 3.5 + es7 + nginx + https](./docker/docker/thehive35-es7-nginx-https) by [@aacgood](https://github.com/aacgood) 
#### Thehive 3.4 (Elasticsearc 6)

- [TheHive 3.4 + Cortex 3.0 + ES 6 + Traefik + Route53](./docker/thehive34-cortex3-es6-traefik-route53) by [@aacgood](https://github.com/aacgood) 
- [TheHive 3.4 + es6 + nginx + https](./docker/docker/thehive34-es6-nginx-https) by [@aacgood](https://github.com/aacgood) 

## TODO

The list bellow includes the docker-compose configurations to be done:

- [ ] TheHive 3 + Elasticsearch
- [ ] TheHive 4 + BerkleyDB
- [ ] TheHive 4 + Cassandra
- [ ] Cortex 3 + dockerized neurons
- [ ] Cortex 3 + local neurons
- [ ] Add reverse proxy
  - [ ] Caddy?
  - [ ] Nginx ?
  - [ ] Traefik ?
- [ ] Add oauth providers
  - [ ] keycloak ?
  - [ ] Fusionauth ?


# Contributing
Please see our [Code of conduct](code_of_conduct.md). We welcome your contributions. Please feel free to fork the code, play with it, make some patches and send us pull requests via [issues](https://github.com/TheHive-Project/TheHive/issues).

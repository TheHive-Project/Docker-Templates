<div>
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-2-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->
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
      <img src="https://img.shields.io/docker/pulls/thehiveproject/thehive?color=%23f8c218&label=Thehive%20docker%20pulls" alt="TheHive Docker pulls">
    </a>
    <a href="./LICENSE" target"_blank">
      <img src="https://img.shields.io/docker/pulls/thehiveproject/cortex?color=%2347b7b7&label=Cortex%20docker%20pulls" alt="Cortex Docker pulls">
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

## Configuration

For the sake of simplicity, the provided docker-compose templates are made simple, without providing the full configuration options of each docker image.

We provide a documentation page for main image used by the templates. For the full docker image options, you need to rely on the image's official documentation.

- [Elasticsearch image configuration](./docs/elasticsearch-config.md)
- [Cassandra image configuration](./docs/cassandra-config.md)
- [TheHive image configuration](./docs/thehive-config.md)
- [Cortex image configuration](./docs/cortex-config.md)
- [NGinx image configuration](./docs/nginx-config.md) 

## Available templates

### Basic templates

- [TheHive 4 + BerkleyDB](./docker/thehive4-berkleydb)
- [TheHive 4 + Cassandra](./docker/thehive4-cassandra)
- [TheHive 3.5 + Cortex 3.1](./docker/thehive35-cortex3-es7)
- [Cortex 3 with dockerized neurons](./docker/cortex3-docker-neurons)

### Custom templates

#### TheHive

- [TheHive 4 + Cassandra + Traefik + Route53](./docker/thehive4-cassandra3-traefik-route53)
- [TheHive 3.5 + es7 + nginx + https](./docker/docker/thehive35-es7-nginx-https)
- [TheHive 3.4 + es6 + nginx + https](./docker/docker/thehive34-es6-nginx-https)

#### Thehive + Cortex

- [TheHive 4 + Cortex 3.1 + MISP 2.4.134 + Shuffle 0.8.0](./docker/thehive4-cortex3-misp-shuffle)
- [TheHive 3.5 + Cortex 3.1 + ES 7 + Traefik + Route53](./docker/thehive35-cortex3-es7-traefik-route53)
- [TheHive 3.5 + Cortex 3.1 + ES 7 + Nginx](./docker/thehive35-cortex3-es7-nginx-https)
- [TheHive 3.4 + Cortex 3.0 + ES 6 + Traefik + Route53](./docker/thehive34-cortex3-es6-traefik-route53)
- [TheHive 3.4 + Cortex 3.0 + ES 6 + Nginx](./docker/thehive34-cortex3-es6-nginx-https)

## TODO

The list bellow includes the docker-compose configurations to be done:

- [x] TheHive 3 + Elasticsearch
- [X] TheHive 4 + BerkleyDB
- [x] TheHive 4 + Cassandra
- [x] Cortex 3 + dockerized neurons
- [ ] Cortex 3 + local neurons
- [ ] Add reverse proxy
  - [ ] Caddy?
  - [x] Nginx ?
  - [ ] Traefik ?
- [ ] Add oauth providers
  - [ ] keycloak ?
  - [ ] Fusionauth ?
# Contributing
Please see our [Code of conduct](code_of_conduct.md). We welcome your contributions. Please feel free to fork the code, play with it, make some patches and send us pull requests via [issues](https://github.com/TheHive-Project/TheHive/issues).

## Contributors ✨

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://strangebee.com/"><img src="https://avatars2.githubusercontent.com/u/21827?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Nabil Adouani</b></sub></a><br /><a href="https://github.com/TheHive-Project/Docker-Templates/commits?author=nadouani" title="Code">💻</a> <a href="https://github.com/TheHive-Project/Docker-Templates/commits?author=nadouani" title="Documentation">📖</a> <a href="https://github.com/TheHive-Project/Docker-Templates/pulls?q=is%3Apr+reviewed-by%3Anadouani" title="Reviewed Pull Requests">👀</a> <a href="https://github.com/TheHive-Project/Docker-Templates/commits?author=nadouani" title="Tests">⚠️</a></td>
    <td align="center"><a href="https://github.com/garanews"><img src="https://avatars1.githubusercontent.com/u/16938405?v=4?s=100" width="100px;" alt=""/><br /><sub><b>garanews</b></sub></a><br /><a href="https://github.com/TheHive-Project/Docker-Templates/commits?author=garanews" title="Code">💻</a> <a href="https://github.com/TheHive-Project/Docker-Templates/commits?author=garanews" title="Documentation">📖</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
[![All Contributors](https://img.shields.io/badge/all_contributors-3-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://blog.agood.cloud"><img src="https://avatars2.githubusercontent.com/u/28122532?v=4" width="100px;" alt=""/><br /><sub><b>aacgood</b></sub></a><br /><a href="https://github.com/TheHive-Project/Docker-Templates/commits?author=aacgood" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/milesflo"><img src="https://avatars1.githubusercontent.com/u/14067660?v=4" width="100px;" alt=""/><br /><sub><b>Miles Florence</b></sub></a><br /><a href="https://github.com/TheHive-Project/Docker-Templates/commits?author=milesflo" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/garanews"><img src="https://avatars1.githubusercontent.com/u/16938405?v=4" width="100px;" alt=""/><br /><sub><b>garanews</b></sub></a><br /><a href="https://github.com/TheHive-Project/Docker-Templates/commits?author=garanews" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

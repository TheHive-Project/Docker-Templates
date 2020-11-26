# thehive3-es6-nginx-https

:warning: Elasticsearch 6 is deprecated and TheHive 3.4.x is no longer maintained.  Consider using TheHive 3.5+ with Elasticsearch 7.

This is a docker-compose configuration to run a TheHive 3.4.4 + Cortex 3.0.1 instances with an Elasticsearch 6.8.8 database backend.  Nginx 1.19.5 is used as reverse proxy in which you supply your own ssl certificates.

Elasticsearch storage has not been configured as persistent in this docker-compose file.

## Usage

```bash
docker-compose up -d
```

## Volume Configuration

- Local files stored in `./vol/nginx` are mapped to the container under `/etc/nginx/conf.d`.  
- Local files stored in `./vol/ssl` are mapped to the container under `/etc/ssl`.  

## TODO

The following items require your attention:

- [ ] Update `thehive.conf` file as appropriate for your requirements
  - [ ] Update `server_name` for your fqdn
  - [ ] Review/modify the configuration for your requirements
- [ ] Add your certificates to `./vol/ssl`
- [ ] Update `./vol/nginx/certs.conf` with the certificate file names
- [ ] Add persistent storage for Elasticsearch

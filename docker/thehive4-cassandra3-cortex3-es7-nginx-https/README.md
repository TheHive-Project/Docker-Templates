# thehive4-cassandra3-cortex3-es7-nginx-https

This is a docker-compose configuration to run a TheHive 4.0.1-2 + Coretex 3.1.0 instances with a Cassandra 3.1.1 database backend for TheHive and Elasticsearch 7.8.1 backend for Cortex.

## .env File

Populate the .env with the following entries.  

| variable              | entry                                         |
|-----------------------|-----------------------------------------------|
| CORTEX_KEY            | API KEY OF CORTEX USER - POPULATED POST SETUP |
| JOB_DIRECTORY         | DIRECTORY TO STORE JOB FILES                  |

## Usage

```bash
docker-compose up -d
```

## Volume Configuration

- Local files stored in `./vol/nginx` are mapped to the container under `/etc/nginx/conf.d`.  
- Local files stored in `./vol/ssl` are mapped to the container under `/etc/ssl`.  
- TheHive `application.conf` file stored in `./vol/thehive/application.conf` is mapped to the container as `/etc/thehive/application.conf`.
- Data for TheHive is stored under `./vol/thehive/data` and is automatically created.
- Data for Elasticsearch is stored under `./vol/elasticsearch` and is automatically created, but may require folder ownership is corrected.
- Data for Cassandra is stored under `./vol/cassandra_data` and is automatically created.

## Known Issues

If the `elasticsearch` container fails to start correctly, or constantly crashes, ensure that the folder ownership is set to the user that ran `docker-compose`.  

This can be corrected by running the following command:

```bash
chown -R 1000:1000 <path_to_elasticsearch>
```

Followed by restarting the `elasticsearch` node with:

```bash
docker-compose up -d elasticsearch
```

## TODO

The following items require your attention:

- [ ] Update `thehive.conf` and `cortex.conf` files for nginx as appropriate
  - [ ] Update `server_name` for your fqdn
  - [ ] Review/modify the configuration for your requirements
- [ ] Add your certificates to `./vol/ssl`
- [ ] Update `./vol/nginx/certs.conf` with the certificate file names
- [ ] Update `.env` with the `CORTEX_KEY` after Cortex has been setup and configured.  A restart of TheHive node is required.

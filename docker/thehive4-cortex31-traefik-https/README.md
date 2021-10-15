# thehive4-cassandra3-cortex3-traefik-https

This is a docker-compose configuration to run latest TheHive4 + latest Cortex instances with a Cassandra 3.1.1 database backend for TheHive and Elasticsearch 7.8.1 backend for Cortex.   
Traefik v2.5 act as a reverse proxy for TheHive and Cortex.   
Traefik is configured with TLS entrypoints with certificate that expires @ year 2042.

## Usage

### Starting stack for first time
```bash
docker-compose up -d
```

### Configuration
After the stack is up and running navigate to [Cortex](https://cortex.localtest.me) and update database + create admin account. Login with admin account and create API-user for hive. Create API-key to that user and copy API-key to the clipboard. Replace `GET THIS FROM CORTEX` in file `./vol/thehive/application.conf` with that API-key   

```bash
play.modules.enabled += org.thp.thehive.connector.cortex.CortexModule
cortex {
  servers = [
    {
      name = local
      url = "http://cortex:9001"
      auth {
        type = "bearer"
        key = "GET THIS FROM CORTEX"
      }
    }
  ]
}
```

and restart stack.
```bash
docker-compose restart
```

### Replacing TLS certificate
One can change TLS-certificates with "legit" certs or generate own self-signed certs with command   
```bash
openssl req -new -newkey rsa:4096 -x509 -sha256 -days 7300 -nodes -out ./vol/traefik/certs/server.cer -keyout ./vol/traefik/certs/private.key
```

## Volume Configuration

- TheHive `application.conf` file stored in `./vol/thehive/application.conf` and it's mapped to the container as `/etc/thehive/application.conf`.   
- Cortex `application.conf` file stored in `./vol/cortex/application.conf` and it's mapped to the container as `/etc/cortex/application.conf`.   
- TLS certificates are stored in `./vol/traefik/certs` and mapped to the container as `/etc/certs/`.   
- Traefik configuration files are stored in `./vol/traefik/conf/` and are mapped to the container as `/etc/traefik/dynamic/`.   
- Data for TheHive is stored under `./vol/thehive/data` and is automatically created.   
- Data for Elasticsearch is stored under `./vol/elasticsearch` and is automatically created, but may require folder ownership is corrected.   
- Data for Cassandra is stored under `./vol/cassandra_data` and is automatically created.   

## Service links
> Services are located in localtest.me domain which is pointing default to 127.0.0.1 (localhost)   
> More information about localtest can be found here: [Localtest.me](https://readme.localtest.me/)
- [Thehive](https://thehive.localtest.me)
- [Cortex](https://cortex.localtest.me)
- [Traefik Dashboard](http://localtest.me:8080)

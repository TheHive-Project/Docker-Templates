# thehive4-cassandra3-traefik-route53

This is a docker-compose configuration to run a TheHive 4.0.1-2 instance with a Cassandra 3.1.1 database backend.

## .env File

Populate the .env with the following entries.  

| variable              | entry                                         |
|-----------------------|-----------------------------------------------|
| AWS_HOSTED_ZONE_ID    | YOUR ROUTE53 DNS ZONE ID                      |
| AWS_ACCESS_KEY_ID     | AWS ACCESS KEY FOR A ROUTE53 USER             |
| AWS_SECRET_ACCESS_KEY | AWS SECRET ACCESS KEY FOR A ROUTE53 USER      |
| LE_EMAIL              | YOUR EMAIL ADDRESS FOR LETS ENCRYPT           |
| TRAEFIK_HOST          | THE FQDN OF THE TRAEFIK CONSOLE               |
| THEHIVE_HOST          | THE FQDN OF THEHIVE WEB GUI                   |

## Usage

```bash
docker-compose up -d
```

## FAQ

Q: My certificates have been issued against `Fake LE Intermediate X1` and come up as invalid.  

A: While testing, to avoid excessive certificate requests the test certificates are used.  To fix this, comment out the line marked `- --certificatesResolvers.mytlschallenge.acme.caServer=https://acme-staging-v02.api.letsencrypt.org/directory`

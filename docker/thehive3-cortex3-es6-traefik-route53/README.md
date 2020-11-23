# thehive3-cortex3-es6-traefik-route53

This is a docker-compose configuration to run a TheHive 3.4.4 + Cortex 3.0.1 instances with an Elasticsearch 6.8.8 database backend.

Elasticsearch storage has not been configured as persistent in this docker-compose file.

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
| CORTEX_HOST           | THE FQDN OF CORTEX WEB GUI                    |
| CORTEX_KEY            | API KEY OF CORTEX USER - POPULATED POST SETUP |

NOTE: You need to configure Cortex to generate the required API KEY.  Once you have created the API KEY you need to rerun `docker-compose up -d`.

## Usage

```bash
docker-compose up -d
```

## FAQ

Q: My certificates have been issued against `Fake LE Intermediate X1` and come up as invalid.  

A: While testing, to avoid excessive certificate requests the test certificates are used.  To fix this, comment out the line marked `- --certificatesResolvers.mytlschallenge.acme.caServer=https://acme-staging-v02.api.letsencrypt.org/directory`

## References

- [blog.agood.cloud - TheHive in Docker](<https://blog.agood.cloud/posts/2020/05/07/thehive-in-docker/>)

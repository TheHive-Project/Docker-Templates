## TheHive 4 + Cortex 3.1 + NodeRED template

This template is used to showcase the integration of TheHive and Cortex with [NodeRED](https://nodered.org)

- Run the docker compose template `docker-compose up -d`
- On `http://locahost:9001`, create a Cortex organisation and a user with an API Key
- Copy the API key and set it in `vol/thehive/application.conf` to configure Cortex module
- Restart the docker compose template `docker-compose down && docker-compose up -d`
- Access to TheHive `http://localhost:9000`
- Access to NodeRED `http://localhost:1880`

Enjoy
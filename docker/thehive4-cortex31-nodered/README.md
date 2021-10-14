## TheHive 4 + Cortex 3.1 + NodeRED template

This template is used to showcase the integration of TheHive and Cortex with [NodeRED](https://nodered.org)

## Steps 
- Run the docker compose template `docker-compose up -d`
- On `http://locahost:9001`, create a Cortex organisation and a user with an API Key
- Copy the API key and set it in `vol/thehive/application.conf` to configure Cortex module
- Enable Node-Red webook [TheHive docs](https://docs.thehive-project.org/thehive/installation-and-configuration/configuration/webhooks/)
- Restart the docker compose template `docker-compose down && docker-compose up -d`

## Access to services
- Access to TheHive `http://localhost:9000`
- Access to Cortex `http://localhost:9001`
- Access to NodeRED `http://localhost:1880`

Enjoy
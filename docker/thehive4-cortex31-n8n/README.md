## TheHive 4 + Cortex 3.1 + n8n template

This template is used to showcase the integration of TheHive and Cortex with [n8n.io](n8n.io)

- Run the docker compose template `docker-compose up -d`
- On `http://locahost:9001`, create a Cortex organisation and a user with an API Key
- Copy the API key and set it in `vol/thehive/application.conf` to configure Cortex module
- Restart the docker compose template `docker-compose down && docker-compose up -d`
- Access to TheHive `http://localhost:9000`
- Access to n8n `http://localhost:5678`

Use `http://thehive:9000` and `http://cortex:9001` in n8n UI when defining credentials nodes.

Enjoy


## Docs

- [Cortex node documentation](https://docs.n8n.io/nodes/n8n-nodes-base.cortex/#basic-operations)
- [TheHive node documentation](https://docs.n8n.io/nodes/n8n-nodes-base.theHive/#example-usage)
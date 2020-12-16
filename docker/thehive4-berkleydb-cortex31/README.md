## TheHive 4 + Cortex 3.1

This template is used to showcase a simple TheHive and Cortex integration

### pre-required (mac user)

You need to add path `/opt/cortex/jobs` to sharing folder on preference Docker

### process install

-   Run the docker compose template `docker-compose up -d`
-   On `http://locahost:9001`, click to update dataBase
-   Connect you with admin user (default user: `admin@thehive.local`, password: `secret`) and create a Cortex organisation and a user with an API Key
-   Copy the API key and set it in `vol/thehive/application.conf` on `key = "API_KEY_HERE"` to configure Cortex module
-   Restart the docker compose template `docker-compose down && docker-compose up -d`
-   Access to TheHive `http://localhost:9000` (default user: `admin@thehive.local`, password: `secret`)
-   Access to Cortex `http://localhost:9001`

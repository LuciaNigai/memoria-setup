## Memoria – Dockerized Microservices Setup

This repository contains a docker-compose.yaml file to set up and run four services that are part of the Memoria application.
### Prerequisites

Docker must be installed on your machine to run the application in a production-like environment using containers.

### How to Run the App

1. Create a folder — this will serve as the parent directory for the entire app.

2. Clone this repository into that folder.

3. Inside the same folder, clone the following repositories:

https://github.com/LuciaNigai/memoria-gateway

https://github.com/LuciaNigai/memoria-auth

https://github.com/LuciaNigai/memoria-data

https://github.com/LuciaNigai/memoria-training


Your directory structure should now look like this:

    /your-app-folder
    ├── memoria-auth
    ├── memoria-data
    ├── memoria-gateway
    ├── memoria-training
    └── docker-compose.yaml

### Configuration

This repository contains a .env_template file with default environment variables.

You can rename this file to .env to use it as-is.

For security or customization, feel free to modify it before renaming.

_**!** If you're running the app with the dev profile (e.g., in an IDE), and you've made changes to .env, make sure to also update the dev.env file in your services to match._

### Start the App

In the parent folder (where docker-compose.yaml is located), run:

```shell
docker compose up
```

This will build and start all Memoria services via Docker.
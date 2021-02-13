# App-Minio

## First Time Prerequisites

1. Run [Traefik](https://github.com/HackingServerHomelab/App-Traefik)

## Running the Containers

1. Update the following volumes in [docker-compose.yml](./Docker/docker-compose.yml)
    * `../Data/minio:/data`
1. Update the following environment variables in [docker-compose.yml](./Docker/docker-compose.yml)
    * `MINIO_ACCESS_KEY=changeme`
    * `MINIO_SECRET_KEY=changeme`
2. Update the Traefik host label in [docker-compose.yml](./Docker/docker-compose.yml)
    * ``"traefik.http.routers.minio.rule=Host(`localhost`)"``
3. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip>

# docker-overrides-tutorial
Share Compose configurations between files and projects

## Running normally
When you run `docker-compose up` it reads the overrides in `docker-compose.override.yml` automatically.

## Running on production
To deploy with the production Compose file you can run;

- `docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d`
  
This deploys all three services using the configuration in `docker-compose.yml` and `docker-compose.prod.yml` (but not the dev configuration in `docker-compose.override.yml`).

See [docker production](https://docs.docker.com/compose/production/) for more information about Compose in production.

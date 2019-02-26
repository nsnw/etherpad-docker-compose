# etherpad-docker-compose

This is a `docker-compose` configuration for Etherpad. It builds on the existing `Dockerfile` that can be found at https://github.com/ether/etherpad-docker.

This will start up a Postgres container and an Etherpad container configured to use Postgres, listening on port 9001. SSL is left unconfigured, with the intention of putting this behind Apache or NginX.

## Customising

The default configuration for Postgres sets up a database named `etherpad`, with a user of `etherpad` and a password of `changeme`. To change this:-

* update the configuration in settings.json (the `dbSettings` section)
* update the configuration in `docker-compose` (the `POSTGRES_*` variables)
* rebuild the Etherpad image with `docker-compose build`

For more information, consult the Etherpad documentation at https://github.com/ether/etherpad-lite/wiki/.

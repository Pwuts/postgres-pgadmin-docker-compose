Postgres + pgAdmin docker config
================================

This is an easy to use docker configuration to set up postgres and pgAdmin.

### Provides
* a Postgres 14 instance
* a pgAdmin 6 instance (bound to port `8032`)
* a docker network named `postgres`

### Usage
1. Clone this repo
2. Copy `example.env` -> `.env` and adjust variables if necessary
3. Run `setup.sh` to fix permissions (this may need elevated permissions to run)
4. `docker-compose up`
5. Add any containers which need access to postgres to the `postgres` network

Containers in the `postgres` network can reach the database at `postgres:5432`.
pgAdmin is accessible on host port `8032`.

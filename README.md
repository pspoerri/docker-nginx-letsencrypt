# NGINX Static Website 

Integrates into the [docker-compose-letsencrypt-nginx-proxy-companion](https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion).

## How to use it

1. Setup the [docker-compose-letsencrypt-nginx-proxy-companion](https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion)
2. Clone the repository `git clone https://github.com/pspoerri/docker-nginx-letsencrypt.git`

3. Make a copy of `.env.sample`, rename it to `.env` and adapt it to your needs.
```
# The name of the container
CONTAINER_NAME=nginx-static-www
# Web proxy as defined in https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion
NETWORK=webproxy
# Static data directory
DATA_DIR=/data/dir/you/would/like/to/serve
# Domain
DOMAINS=example.com
# For multiple domains specify a list of domains with commas
# DOMAINS=example1.com,example2.com
LETSENCRYPT_EMAIL=domain@example.com
```
4. Start nginx by running `./start.sh`

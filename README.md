# RHoMIS 2.0 Data Server

An easy to set-up server to manage processed data,
users, data-access.

Has only been tested on Ubuntu 20.04.

# Setup

* Install docker and docker compose.
* Enter the command `cp ./templates/.env.template .env` to create your .env file. Replace the default values with the values  relevant to your server.
* Add your credentials to the configuration files by entering the command `source configure.sh`
* Install the software you need by entering the following command `source install.sh`
* Get the service up and running with `docker-compose up -d rhomis-api-server`.
* Create self-signed certificates to allow the nginx container to start with the `source init-letsencrypt.sh` 
* Finally build the server with the command `docker-compose build` and start it with the command `docker-compose-up`


# Useful links

* Build using [this tutuorial](https://pentacent.medium.com/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71) and [this tutorial](https://www.digitalocean.com/community/tutorials/how-to-secure-a-containerized-node-js-application-with-nginx-let-s-encrypt-and-docker-compose)
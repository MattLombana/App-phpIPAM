# App-phpIPAM

## First Time Prerequisites

1. `rm ./Data/mysql/.gitkeep`
2. Run [Traefik](https://github.com/mattlombana/App-Traefik)

## Running the Containers

1. Update the following lines in [docker-compose.yml](./Docker/docker-compose.yml)
    * `MYSQL_ROOT_PASSWORD=example`
2. Update the Traefik host label in [docker-compose.yml](./Docker/docker-compose.yml)
    * ``"traefik.http.routers.phpipam.rule=Host(`localhost`)"``
3. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip>
2. Click "New phpipam installation" then "Automatic database installation"
2. Create a new database, use the username `root` and the password you set with `MYSQL_ROOT_PASSWORD`
3. Create an admin password and set the title and Site URL
4. Log in and configure any other settings with the username `Admin` and the
   password you just created

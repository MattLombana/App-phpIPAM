# App-phpIPAM

## First Time Prerequisites

1. `rm ./Data/example/.gitkeep`

## Running the Containers

1. Run `./Config/gen_certs.sh` to generate the SSL certificates (alternatively,
   add custom certs to the private folder)
2. Update the `server_name` in [nginx.conf](./Config/nginx.conf)
3. Update the following lines in [docker-compose.yml](./Docker/docker-compose.yml)
    * `MYSQL_ROOT_PASSWORD=example`
4. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip>
2. Click "New phpipam installation" then "Automatic database installation"
2. Create a new database, use the username `root` and the password you set with `MYSQL_ROOT_PASSWORD`
3. Create an admin password and set the title and Site URL
4. Log in and configure any other settings with the username `Admin` and the
   password you just created

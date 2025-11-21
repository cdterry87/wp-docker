> This repository contains a Docker configuration for developing a Wordpress site with an Apache web server and MySQL database.
>
> NOTE: This is not a production ready Docker configuration. It is for development purposes only.

## Requirements

Make sure Docker is installed in your development environment. You may also install Docker Desktop if you prefer a GUI.

## Usage

To use this repository, follow the following steps:

1. Clone it to your environment using `git clone https://github.com/cdterry87/wp-docker`. Then `cd` to the `wp-docker` directory you just created.
   > NOTE: Optionally you. may run `git clone https://github.com/cdterry87/wp-docker my-project-name` to create a named project directory.
2. In the `.env` file set the `PROJECT_NAME` to whatever your project is named.
   > NOTE: This will also set the name of your containers/database so don't use spaces or special characters.
3. In the `.env` file you may also set the database credentials as needed or leave the defaults for your development environment.
4. Run the following command to build the Docker container and start it: `docker-compose up --build -d`
   > NOTE: If `docker-compose` doesn't work, try `docker compose` instead.
5. Visit `http://localhost:8000` in your browser and you should see your Wordpress site! Follow the installation instructions to setup your Wordpress site like normal.
6. To bring down the container, use the following command: `docker-compose down`
   > NOTE: If you bring the container up again your data should still be intact.
7. To destroy the container, use the following command: `docker-compose down -v`
   > NOTE: If you destroy a container this way the data is not recoverable.

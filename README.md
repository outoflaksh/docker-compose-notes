# Let's learn Docker Compose!

## What is Docker?

Docker is an open-source platform that helps you package your applications into containers. It helps containerizing, deploying and managing your software projects with a set of tools like the Docker engine, Docker images, Dockerfiles, and Docker Compose.

## What is Docker Compose?

Docker Compose is a Docker tool to run multiple Docker container instances. It simplifies the process of managing and orchestrating multiple Docker container instances as a single unit.

Using a YAML file, you can specify the services, networks, volumes, and other configurations required for your application. Docker Compose then takes care of creating and managing the necessary containers, setting up the network connections between them, and ensuring they communicate effectively.

By using Docker Compose, you can define the relationships and dependencies between different containers, making it easier to deploy and manage complex applications that consist of multiple interconnected services.

## docker-compose.yaml - Where the magic happens!

This YAML file configures a Docker Compose instance. This should ideally be created inside a project directory and saved at the root.

The file starts of with a line that defines the version, then under the `services` section, one can define all their Docker container services and each of their propertiessuch as the Docker image to use, environment variables, ports to expose, volume mounts, network configurations, and more.

To start a Docker Compose session, run this command:
`docker-compose up`

And to stop the session, simply run:
`docker-compose stop`

Run the above commands at the root of the directory, where the `docker-compose.yaml` file is located.

You can add the flag `-d` after the up command to run the container in background:
`docker-compose up -d`

To completely remove the containers, use:
`docker-compose down`

## Basic building blocks of a docker-compose file

Here are some useful sections of a docker-compose config file:

- `version` defines the version
- `services` define all your containers under this
- `networks` define your Docker networks
- `environment` define the env vars for a container
- `ports` expose the ports needed for a container service
- `image` defines the Docker base image to use

### Run a sample wordpress container

To run a local version of a Wordpress instance on your machine, follow the steps:
- Make a directory
- At the root of that directory, add my [sample docker-compose config file]("https://github.com/outoflaksh/docker-compose-notes/blob/main/wordpress-example/docker-compose.yaml").
- Run the command `docker-compose up` at the root of the created directory.
- Go to `localhost:8081` and voila!✨

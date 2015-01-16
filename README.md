# Strider Vagrant

## Intriduction

This is a [Vagrant](https://www.vagrantup.com/) box that runs [Strider-CD](https://github.com/Strider-CD/strider) and [docker](https://www.docker.com/) to enable local CI/CD that runs in a background and builds you local git pushes before hitting the main build server.

## Usage

```sh
$ vagrant up
```

Simple as that.

Hit the server at `http://localhost:3001`

## Docker image

We maintain a custom pimped docker image for Strider [here](https://github.com/eneset/strider-docker-slave) and push it to docker hub.

If you want to play with the image, pull it from the docker hub.

```sh
$ docker pull eneset/strider-docker-slave
```

Otherwise just use `eneset/strider-docker-slave` in your Strider setup and it will be pulled automatically.

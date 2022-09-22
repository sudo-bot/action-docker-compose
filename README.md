# A GitHub action to run docker-compose

Go to [docker-compose](https://github.com/koalaman/docker-compose#readme) at GitHub

You can find the image on [Docker Hub](https://hub.docker.com/r/botsudo/action-docker-compose)

[![Docker Pulls](https://img.shields.io/docker/pulls/botsudo/action-docker-compose.svg)](https://hub.docker.com/r/botsudo/action-docker-compose)

I use the base image [docker/compose](https://hub.docker.com/r/docker/compose) for this action

## Example usage

```yml
  - uses: actions/checkout@v3
  - name: run docker-compose
    uses: sudo-bot/action-docker-compose@latest
    with:
        # https://docs.docker.com/compose/reference/overview/
        cli-args: "up"
```

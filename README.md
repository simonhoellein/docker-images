# Multi-Platform docker images

This is a template for building multi-platform docker images with a github actions CI/CD Pipeline and pushing them to docker-hub

## How to use this?

1. Create a new repo with this template
2. Create a Repository Secret `DOCKER_KEY` for your docker-hub API Key
3. Create a Repository Variable `DOCKER_USER` for your docker username
4. Create a dockerfile in the root of this repo and let the pipeline build and push it :)

## Info

- The pipelines uses the variable `GITHUB_REPOSITORY` as a value for things like the docker image and push destination. This works as long as your github username is the same as the username in docker-hub. The benefit of doing this is, that you don't have to edit the pipeline at all because the name for the docker images is determined by the repo name in github. For example: If I create a repo called `simonhoellein/actions-runner` the docker image will be published to <https://hub.docker.com/r/simonhoellein/actions-runner>.

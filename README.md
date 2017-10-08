# Docker Compose

This docker image installs docker-compose and ssh-agent on top of the `docker` image.
This is very usefull for CI pipelines, which leverage "Docker in Docker".

## Docker versions supported

There are versions based on different docker versions, e.g. `latest`, `17.06`, `17.03` and `1.13`.

## Usage instructions for GitLab CI

You may use it like this in your `.gitlab-ci.yml` file.

```yaml
image: louisbb/docker-compose-ssh:latest

# Optional
services:
  - docker:dind

before_script:
  - docker info
  - docker-compose --version

build image:
  stage: build
  script:
    - docker-compose build
```

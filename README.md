# usage

```
steps:
  - command: '<optional script to run in service>'
    plugins:
      - 'albertywu/run-docker-compose':
        compose-file: '<PATH TO DOCKER COMPOSE FILE>'
        image: '<ECR IMAGE>'
        package: '<WEB_CODE PACKAGE>'
        service: '<SERVICE>'
```

# example

```
steps:
  - command: path/to/script.sh
    plugins:
      - 'albertywu/run-docker-compose':
        compose-file: 'projects/monorepo-tools/scripts/docker/docker-compose.yml'
        image: '<ecr image from previous build step>'
        package: 'projects/example-trips-viewer-fusion'
        service: 'web-code-run'
```
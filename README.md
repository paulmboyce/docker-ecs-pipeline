# Welcome to your CDK TypeScript project

This is a blank project for CDK development with TypeScript.

The `cdk.json` file tells the CDK Toolkit how to execute your app.

## Useful commands

* `npm run build`   compile typescript to js
* `npm run watch`   watch for changes and compile
* `npm run test`    perform the jest unit tests
* `cdk deploy`      deploy this stack to your default AWS account/region
* `cdk diff`        compare deployed stack with current state
* `cdk synth`       emits the synthesized CloudFormation template

# Running Containers

## [DOCKER]:

cd into the /app folder

```
$ docker build . -t app/v1
```

## [DOCKER COMPOSE]:

### Install
SEE https://docs.docker.com/compose/install/linux/

```
$ DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
$ mkdir -p $DOCKER_CONFIG/cli-plugins
$ curl -SL https://github.com/docker/compose/releases/download/v2.17.2/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
$ chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
$ docker compose version
 Docker Compose version v2.17.2
```

```
$ docker compose build --no-cache
$ docker compose up
```

Docker compose tails logs

## Check Containers:
```
$ docker ps
```

## Tail Container Logs:
List processes to get the image id, thne use id to tail
```
$ docker ps
$ docker logs 12345567 --follow
```

## Run Docker Compose in Watch Mode [Experimental]

SEE: https://www.docker.com/blog/docker-compose-experiment-sync-files-and-automatically-rebuild-services-with-watch-mode/

````
$ docker compose build && docker compose up --wait  && docker compose alpha watch
`````

NOTE: rebuild causes a full restart.  Can use rebuild or sync. 
Sync works to copy files, but node does not restart the service if edit index.js.

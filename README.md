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
```
$ docker-compose build --no-cache
$ docker-compose up
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

# Repo to demo a [bug report](https://github.com/prismagraphql/prisma/issues/2642#issuecomment-398321457) for prisma

## Versions

Node 10.4.1
Prisma CLI 1.10
macOS 10.13.5

Tested using a hosted postgres database on compose.io

## Additional Context

This repo is in a functional state.

In docker-compose.yml replace __MY_HOST__ with your host and __MY_PORT__ with your port etc...

To deploy run the following commands

`docker-compose up -d`

`prisma deploy`

## To Reproduce Bug

- Remove the stage and service keys in the `prisma.yml` file such that the contents of the file are

```
endpoint: http://localhost:4466
datamodel: datamodel.graphql
```

- Build docker container `docker-compose up -d`
- deploy prisma `prisma deploy`

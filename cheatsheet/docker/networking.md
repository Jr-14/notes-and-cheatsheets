# Getting started
`DRIVER` accepts eithers `bridge` or `overlay` which are built-in ***network drivers***.

`DRIVER` defaults to `bridge` network.

[Multiple compose files](https://docs.docker.com/compose/multiple-compose-files/)

[Networking in Compose](https://docs.docker.com/compose/networking/)

`HOST_PORT`:`CONTAINER_PORT`

For example:
```
services:
  web:
    build: .
    ports:
      - "8000:8000"
  db:
    image: postgres
    ports:
      - "8001:5432"
```

`HOST_PORT` is exposed to the local network and accessible outside the docker network
`CONTAINER_PORT` is exposed within the container only

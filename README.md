# reproduce-haproxy-websocket-issue

This repository provides an easy way to reproduce issue on haproxy 2.4.3 with not working websockets when the backend has enabled communication over http/2.

## Prerequisites

* [docker](https://docs.docker.com/engine/install/ubuntu/)
* [docker-compose](https://docs.docker.com/compose/install/)

## How to run

```
docker-compose up --build
```

then check https://localhost:8443/test.html to observe failure and https://localhost:8444/test.html that should print timestamps in random delays as expected. Also https://localhost:9443/test.html is exposed to show that without haproxy everything works as intended.
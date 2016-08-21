# ocr-docker

This repo contains a Docker Compose file that can be used to start up all the apps necessary to run the OCR microservices demo
from my [blog](http://ryanjbaxter.com).  In order to run the containers you will need [Docker](http://docker.com) and 
[Docker Compose](https://docs.docker.com/compose/) installed.

## Running

First clone the repo

`$ git clone https://github.com/ryanjbaxter/ocr-docker`

From the root of the repo run

```
$ cd ocr-docker
$ docker-compose build
$ docker-compose up
```

This will start several Spring Boot apps.

### [OCR Eureka](https://github.com/ryanjbaxter/ocr-eureka)
Eureka server used for service discovery.  Runs on port `8761`.

### [OCR Races](https://github.com/ryanjbaxter/ocr-races)
Serves race data.  Runs on port `8282`.

### [OCR Participants](https://github.com/ryanjbaxter/ocr-participants)
Serves participant data.  Runs on port `8181`.

### [OCR Web](https://github.com/ryanjbaxter/ocr-web)
Servers web content.  Runs on port `8080`.

### [OCR Hystrix Dashboard](https://github.com/ryanjbaxter/ocr-hystrix-dashboard/)
Serves the Hystrix Dashbaord to monitor circuit breakers.  Runs on port `8383`.

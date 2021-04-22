# MQTT-python

## Introduction
This work proposes HOST – a solution that addresses the problems of data heterogeneity and the interoperability of smart objects in the context of a smart home. HOST was modeled to compose a set of intelligent objects to form a computational infrastructure in fog.

 To disseminate heterogeneous information, a Publish/Subscribe communication module was implemented to abstract the details of communication between objects. A performance evaluation was carried out to validate HOST. The results show evidence of efficiency (i) in the computational resources of the devices; and (ii) in the communication infrastructure. Also, HOST provides scalability about the number of devices acting simultaneously, in addition to demonstrating its ability to work with different types of devices.




## How to get it work
Some steps you need to follow to get it worked 

### 1- Get code source

```
$ git clone https://github.com/arturhbs/HOST.git
```
```
$ cd HOST
```

### 2- Running code with docker 
Execute commands below to run publish's and subscribe's code, respectively:

```
$ docker-compose up -d --scale publisher=5 --scale subscriber=2
```

It is possible to change the number of how many services it will work as your wish.

If need to run more than 20 services simultaneously and it gets an error, it is recommended to try:

```
export DOCKER_CLIENT_TIMEOUT=120
export COMPOSE_HTTP_TIMEOUT=120
```

Other solution is to restart Docker and increase Docker CPU and memory

## Debug mode
For access debug mode run follow code to see publisher's debug:

```
$ docker-compose logs -f 
```
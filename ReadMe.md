Overview
---------

Project will create (in docker)

* A single MarkLogic node

Admin account is
* Username: admin
* Password: admin

Prerequisites
-------------

1. docker toolkit installed
2. Java 8 installed
3. Following ports available -
* 8000-8050


Installation steps (once off)
-----------------------------

1. Download MarkLogic-9.0-5.x86_64.rpm (or any other MarkLogic v9 rpm) and copy it to src/main/docker/marklogic
2. Execute (this will download all required docker dependencies to build marklogic image)
```
    docker-compose build   
```
3. Execute (this will download all required gradle dependencies)
```
    ./gradlew build 
```


Server Setup
-------------
1. ./gradlew mlDockerDeploy

Server Start
-------------
1. ./gradlew mlDockerStart

Server Stop
-------------
1. ./gradlew mlDockerStop

Server TearDown
-------------
1. ./gradlew mlDockerTeardown
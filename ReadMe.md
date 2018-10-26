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

Make sure you have created a security template with the name marklogic.local and use that for enabling ssl on ports 8000, 8001 and 8002 before you run a deployment on the machine.


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
1. create certificate template with name 'marklogic.local'
1. Enable SSL on ports 8000-8002 with above certificate name

Deploy Application
-------------
1. ./gradlew mlDeploy

Server Start
-------------
1. ./gradlew mlDockerStart

Server Stop
-------------
1. ./gradlew mlDockerStop

Server TearDown
-------------
1. ./gradlew mlDockerTeardown
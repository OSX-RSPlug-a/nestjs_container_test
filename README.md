# nestjs_container_test
This proejct has the focus on test the nestjs env on a docker structure;

Starting the project with docker:

      docker build -t node-nestjsapp:release-v1 .

      docker image ls

      docker run -d node-nestjsapp:release-v1

      docker ps

See running in the browser:

      docker network ls

      docker network inspect bridge

      curl --verbose 172.17.0.2:3000

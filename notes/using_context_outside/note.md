# Notes

## 1. docker

- Default build context is same location with the Dockerfile
  - To custom, improve performance of build context, we can add .dockerignore

## 2. docker-compose

- Using docker-compose can set difference context and Dockerfile location
- ```.env``` file only can be used when run docker-compose command
- ```command``` in docker-compose file is ```<command>``` in ```docker run <image> <command>```

## 3. ENTRYPOINT, CMD

- ENTRYPOINT: the command will be executed when container start. Ex: ```ENTRYPOINT ["executable","param1","param2"]```
- CMD: can treat as appended arguments for ENTRYPOINT(if existed) when user run container without any argument.
If ENTRYPOINT not existed, CMD has to be started with an executable
- Examples:

  ```Dockerfile
  ENTRYPOINT [ "echo", "parameter1" ]
  CMD [ "Default parameter if user not pass any parameter when run container" ]


  # ex: docker run using_context_outside_test "parameter2" -> print "parameter1 parameter2"
  # ex: docker run using_context_outside_test -> print "parameter1 Default parameter if user not pass any parameter when run container"
  ```

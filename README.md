# docker_ws

Commands:

  Ubuntu:

    - Initialize docker image: sudo docker run --net=host --env="DISPLAY" --volume="$HOME/.Xauthority:/root/.Xauthority:rw" --name <container_name> --privileged  -it <image_name> /bin/bash

    - Create new terminal for a given container: sudo docker exec -it <container_name>
    - Give permissions to docker to display: sudo xhost +local:docker
    - Remove ALL the running containers: sudo docker rm -f $(docker ps -qa)
    - Remove ALL the existing images: sudo docker rmi -f $(docker images -aq)
    
  Windows:
  
    - Initialize docker image: docker run --net=host -e DISPLAY=<ip>:0.0 --name <container_name> --privileged -it <image_name> bash
    
    Important: Fixed IP and MobaXterm installed

Important:

  - Every time a terminal is opened, execute: $ source opt/ros/<ros-distro>/setup.bash

# docker_ws

Commands:

  - Initialize docker image: $ sudo docker run --net=host --env="DISPLAY" --volume="$HOME/.Xauthority:/root/.Xauthority:rw" --name <container_name> -it <image_name> /bin/bash
  - Create new terminal for a given container: $ sudo docker exec -it <container_name>
  - Give permissions to docker to display: $ sudo xhost +local:docker
  - Remove ALL the running containers: $ docker rm -f $(docker ps -qa)
  - Remove ALL the existing images: $ docker rmi -f $(docker images -aq)

Important:

  - Every time a terminal is opened, execute: $ source opt/ros/<ros-distro>/setup.bash

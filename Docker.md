# 基本操作命令

- docker search [name]

    搜索相关镜像，如 docker search mysql

- docker pull [name]

    拉取相关镜像，如 docker pull docker.io/redis

- docker images

    展示本地的镜像列表

- docker tag [name] [new name]

    为本地镜像起个别名，如 docker tag docker.io/centos/mysql-57-centos7 mysql

- docker run [name]

    运行镜像，如 docker run mysql

- docker inspect [name]

    查看镜像详细信息，如 docker inspect mysql

- docker history [name]

    查看镜像的历史信息，如 docker history mysql

- docker ps -a

    查看运行着的容器

- docker rm [name]

    删除容器，如 docker rm 5b41bb88f7e3

- docker rmi [tag]

    根据tag删除镜像，如果有多个tag，仅会删除该tag，如 docker rmi mysql

- docker rmi [id]

    根据id删除镜像，如果该镜像有多个tag，无法删除，如 docker rmi 719cd2e3ed04

    > 删除镜像时，必须保证镜像的容器不在运行

- docker image prune

    清除不使用的镜像
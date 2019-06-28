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

# 容器操作

- docker create [option] [image]

    创建容器，如 docker create -it nginx

- docker start [container]

    启动容器，如 docker start 92f

    ```shell
    [root@iZbp1epntmn4ju75ny9m1uZ ~]# docker create -it nginx
    92f4882b25f4ef46e9734eb700f74d380e601a5e92e83423126c206330a09144
    [root@iZbp1epntmn4ju75ny9m1uZ ~]# docker ps -a
    CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
    92f4882b25f4        nginx               "nginx -g 'daemon ..."   5 seconds ago       Created                                 gracious_ritchie
    [root@iZbp1epntmn4ju75ny9m1uZ ~]# docker start 92f
    92f
    [root@iZbp1epntmn4ju75ny9m1uZ ~]# docker ps -a
    CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES
    92f4882b25f4        nginx               "nginx -g 'daemon ..."   2 minutes ago       Up 6 seconds        80/tcp              gracious_ritchie
    ```

- docker run [option] [name]

    运行镜像，如 docker run -it mysql

- docker pause/unpause [container]

    暂停和继续运行容器

- docker stop  [container]

    给容器标记停止状态，默认情况10s后容器会停止

- docker kill [container]

    直接杀死正在运行中的容器

- docker restart [container]

    重启容器

- docker rm [container]

    删除容器

- docker exec [option] [container] [command]

    当容器以后台模式运行时（-d），进入容器。

    
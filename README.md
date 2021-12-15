At first we need to create a file named "docker.mariadb.service" in the location "/lib/systemd/system"

Once the file is ready use the command

```
# docker container ls -a
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
#

# service docker.mariadb status
● docker.mariadb.service - MariaDB
   Loaded: loaded (/lib/systemd/system/docker.mariadb.service; disabled; vendor preset: enabled)
   Active: active (running) since Wed 2021-12-15 11:37:33 IST; 31s ago
 Main PID: 11257 (docker)
    Tasks: 11
   Memory: 19.4M
      CPU: 140ms
   CGroup: /system.slice/docker.mariadb.service
           └─11257 /usr/bin/docker run --rm --name=mariadb -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=test -e MYSQL_USER=user -
           Dec 15 11:37:42 ismail-hp docker[11257]: 4bbcce26bc5e: Pull complete
Dec 15 11:37:43 -docker[11257]: ef669123e59e: Verifying Checksum
Dec 15 11:37:43  docker[11257]: ef669123e59e: Download complete
Dec 15 11:37:43  docker[11257]: 04f220ee9266: Pull complete
Dec 15 11:37:43  docker[11257]: b14b1ba1d651: Verifying Checksum
Dec 15 11:37:43  docker[11257]: b14b1ba1d651: Download complete
Dec 15 11:37:44  docker[11257]: 89c8a77f7842: Pull complete
Dec 15 11:37:44  docker[11257]: d1de5652303b: Pull complete
Dec 15 11:37:45  docker[11257]: ef669123e59e: Pull complete
Dec 15 11:37:57  docker[11257]: e5cec468d3a6: Download complete
           
# docker container ls -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                    NAMES
4437bd0a571d        mariadb:latest      "docker-entrypoint.s…"   41 seconds ago      Up 35 seconds       0.0.0.0:3306->3306/tcp   mariadb
# 

```

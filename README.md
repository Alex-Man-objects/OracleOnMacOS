# OracleOnMacOS
 This is an Oracle image can be built and Running on MacOS Docker.
 Please make sure Docker is running before step 2.
 ## Step 1.
 get docker images here:
 https://github.com/oracle/docker-images
 
 cd docker-images/OracleDatabase/SingleInstance/dockerfiles

 ## Step 2
 http://www.oracle.com/technetwork/database/enterprise-edition/downloads/index.html
 
 download a oracle database and place it in the equvilent version folder, such as 12.2.0.1, then run below command.

./buildDockerImage.sh -v 12.2.0.1 -e

 ## Step 3
map to local port and data file

docker run --name oracle -p 1521:1521 -p 5500:5500 -v /Users/{user}/idocker/oradata:/opt/oracle/oradata oracle/database:12.2.0.1-ee

## Image is available on Docker Hub:
https://hub.docker.com/repository/docker/zhenzhenman/oracle12

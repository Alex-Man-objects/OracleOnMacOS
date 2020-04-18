# OracleOnMacOS
 This is an Oracle image can be built and Running on MacOS Docker.
 Please make sure Docker is running before step 2.
 ## Step 1.

 cd docker-images/OracleDatabase/SingleInstance/dockerfiles

 ## Step 2

 ./buildDockerImage.sh -v 12.2.0.1 -e

 ## Step 3

 docker run --name oracle -p 1521:1521 -p 5500:5500 -v /Users/Zhenzhen/idocker/oradata:/opt/oracle/oradata oracle/database:12.2.0.1-ee

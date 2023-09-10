\build\docker\oracle\

docker-images\OracleDatabase\SingleInstance\


dockerfilessh biuldDockerImage.sh -v 19.3.0 -s


cd D:\oracle\docker-images\OracleDatabase\SingleInstance\dockerfiles\19.3.0
docker build -t oracle/database:19.3.0.0-se2 .

docker run -d --env-file ./oracle.env -p 1521:1521 -p 5500:5500 -it --name my_oracle --shm-size="4g" oracle/database:19.3.0.0-se2



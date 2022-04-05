#DOCKER
sudo service docker start
docker build -t codeeducation .
docker build --no-cache -t codeeducation .
docker run --name codeeducation -p 8080:80 -tid codeeducation
docker exec -it codeeducation bash
docker rm $(docker ps -aq) -f
docker rmi $(docker images -a -q)
docker images

#Push to docker hub
docker login
docker tag codeeducation:latest arthurranzini/codeeducation:latest
docker push arthurranzini/codeeducation
docker run /codeeducation

#GIT
#REMOTO / ADICIONAR REMOTO
git checkout master
git branch -m main
git status


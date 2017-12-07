# Jenkins docker
* Jenkins CI with docker client

git clone https://github.com/christseng89/jenkins-docker.git
cd jenkins-docker

docker build -t jenkins-docker .
docker rm -f jenkins
docker run -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock --name jenkins -d jenkins-docker

docker exec -it jenkins bash
ls -lah /var/run/docker.sock
# number is important

docker ps -a

# install Jenkins  03-04

docker run -p 3000:3000 -d --name my-nodejs-app christseng89/docker-nodejs-demo
curl localhost:3000


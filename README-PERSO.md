# Personal test

## Run:

`docker run -d -p 8080:8080 -p 50000:50000 -u jenkins:999 --restart=always --name jenkins --hostname jenkins -v /var/run/docker.sock:/var/run/docker.sock -v jenkins:/var/jenkins_home -v jenkins-logs:/var/log/jenkins -e JAVA_OPTS="-Xms1g -Xmx2g" jenkins-lts:2.249.3-lts-ubuntu`

## Build:

Run
 
`docker build -t jenkins-lts:2.277.1-lts-ubuntu --build-arg JENKINS_VERSION=2.277.1 --file 8/ubuntu/bionic/openj9/Dockerfile`
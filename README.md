# Jenkins-integration-with-kubernetes
CI/CD Pipeline for kubernetes deployment using Jenkins

### We assume we have Jenkins instance running if not,spin on up in cloud or follow below steps to run it in docker
`docker run -d -p 8080:8080 -p 50000:50000 -name myjenkins -it -u 0 \
-v /var/run/docker.sock:/var/run/docker.sock \
-v $(which docker):/usr/bin/docker \
-v /home/jenkins_home:/var/jenkins_home \
jenkins/jenkins:latest`
<br />

### Install two plugins in Jenkins
- docker pipeline
- kubernetes continous plugin

#### Add dockerhub credentials in Jenkins
#### Also, add kubernetes config credential
`~/.kube/config`
copy this content into jenkins credential manager
- make sure k8s cluster is running


## Create pipeline in jenkins and point to this repo
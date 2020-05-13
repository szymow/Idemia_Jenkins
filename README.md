# Idemia_Jenkins

https://rangle.io/blog/running-jenkins-and-persisting-state-locally-using-docker-2/

sudo docker volume create jenkins_persistant

sudo docker run --name jenkins-local -p 8080:8080 -p 50000:50000 -v jenkins_persistant:/var/jenkins_home jenkins

docker exec -u root -t -i container_id /bin/bash

Update Jenkins - Ręczna podmiana pliku WAR

#on ubuntu, in /usr/share/jenkins:

sudo service jenkins stop

sudo mv jenkins.war jenkins.war.old

sudo wget https://updates.jenkins-ci.org/latest/jenkins.war

sudo service jenkins start

# Apache Struts - Vulnerable Container
## How to Build the Image from Dockerfile
## Phase1 - Requirements
Linux Machine

### Installing Docker
curl -fsSL https://get.docker.com | sh

## Phase2 - Building the Image

### Cloning GitHub Repo
git clone https://github.com/andrefernandes86/demo-apachestruts-target.git

### Building the Image
docker image build -t demo-apachestruts-target .

## Phase3 - Starting the Container
### Starting the Container
docker run -d --rm --name demo-apachestruts-target -p 80:8080 demo-apachestruts-target

### Executing Commands Inside the Attacker Container
docker exec -it demo-apachestruts-target bash

## Phase4 - Checking the Vulnerable Web App
http://demo-apachestruts-target

## How to Build the Image from DockerHub
### References
docker push andrefernandes86/demo-apachestruts-target
https://github.com/andrefernandes86/demo-apachestruts
https://github.com/andrefernandes86/demo-dvwa
https://raw.githubusercontent.com/andrefernandes86/demo-dvwa/master/commands.txt


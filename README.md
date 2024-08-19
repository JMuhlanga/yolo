# Project overview

This project is a demonstration of the skills involved in Containerization, Deployment, and Orchestration through the DevOps Course Work

## VIA DOCKER - IP2

### Requirements to run the project 
Install the docker engine suitable for your Operating system via 
- [Docker](https://docs.docker.com/engine/install/) 

Install git on your machine 
- [Git](https://git-scm.com/)

### Clone This repository

In order to clone this repository using git in your local machine proceed to run :
```
git clone https://github.com/JMuhlanga/yolo
```

### In order to launch the Application on your machine 

Run 
  ```
  docker-compose up
  ```
### In order to terminate the same application

Run 
  ```
    docker-compose down
  ```

### The Images of this docker Project
Client 
-[Client](https://hub.docker.com/r/jmuhlanga/jmuhlanga-yolo-client)
To pull the same client image via Docker. run:
```
docker pull jmuhlanga/jmuhlanga-yolo-client
```
Back End
-[backend](https://hub.docker.com/r/jmuhlanga/jmuhlanga-yolo-backend)
To Pull the Backend image via Docker, run:
```
docker pull jmuhlanga/jmuhlanga-yolo-backend
```
## VIA Ansible - IP3

### Install Vagrant and Ansible
Installation Instructions
-[Instructions](https://medium.com/@kadimasam/set-up-virtualbox-and-vagrant-on-ubuntu-22-04-9ac6b9ace94c)

### IP3 project Structure

    yolo/
    ├── provisioning/
    │   ├── playbook.yml
    │   ├── vars.yml
    │   ├── hosts
    │   └── roles/
    │       ├── yolo-backend/
    │       │   └──tasks/
    │       │       └── main.yml
    │       │   
    │       ├── yolo-frontend/
    │       │   └── tasks/
    │       │       └── main.yml
    │       │   
    │       └── mongodb/
    │           ├── tasks/
    │           │   └── main.yml
    │           └── files/
    └── Vagrantfile

### Run the Application

In order to run the application, in the root of the project within the terminal kindly run the code below:

```
vagrant up 
```
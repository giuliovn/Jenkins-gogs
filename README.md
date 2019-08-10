# Jenkins-Gogs(+Mysql)

Developement local environment with lightweight Source Control Management (Gogs) backed by Mysql database and CI server (Jenkins) deployed with Docker-compose.

## Getting Started

Create the following directory tree in the project root folder:
```
├── docker-compose.yml
├── db_data/
├── gogs_data/
├── jenkins_home/
```
The directory structure is aimed to preserve data, you may need to manage permissions in order to allow the containers to write in the directories.
The driver network has fixed ip internal address, you may need to modify them if you have other docker projects active in this range.
To start the environment run this command from the root directory of the project:
```
docker-compose up
```

### Gogs setup

For setting up Gogs:

https://github.com/gogs/gogs/tree/master/docker#settings

Default Mysql parameters:
```
      MYSQL_ROOT_PASSWORD: root
      MYSQL_DATABASE: gogs
      MYSQL_USER: gogs
      MYSQL_PASSWORD: gogs
```

### Gogs/Jenkins integration

Install Gogs plugin in Jenkins.
Follow the instruction to configure webhooks:

https://medium.com/@salohyprivat/getting-gogs-and-jenkins-working-together-5e0f21377bcd
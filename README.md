# Jenkins-Compose

## Essential Configs
You need to ensure the directory ~/jenkins exists:
``` 
mkdir ~/jenkins
```
This volume will be used to persist all your data: configurations, plugins, pipelines, passwords, etc.

The remaining two volumes allow you to use docker inside the Jenkins server (Yes, you can create docker containers inside a docker container).

### Run Docker Compose
```
docker-compose up -d
```

### Get the generated Admin Password

```
docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```

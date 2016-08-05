# jenkins-swarm
Docker image of Jenkins with Swarm plugin to be installed in the container start.

## How to use
To run this image, just enter the following command in bash:

```bash
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 jelastic/jenkins-swarm
```

If you want to add JNLP slaves, there is a Docker image that just do the job:  https://github.com/jelastic-jps/jenkins-swarm-slave-docker. Adding them is straighforward, just type in your favorite shell the following command:

```bash
docker run -d --name <the name of your slave> --link jenkins:jenkins jelastic/jenkins-swarm-slave -username jenkins -password jenkins -executors <the number of executors you want>
```

PS: The other arguments in the commands can be changed at your discretion

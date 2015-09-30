HOW TO USE
==========

When you use this container, make sure to have the host
docker socket mounted inside the Jenkins Container using

```
    -v /var/run/docker.sock:/var/run/docker.sock
```

Then the docker client inside the Jenkins Container will be
able to access the container hosts, as if the docker host is
running locally.

```
    docker run -d \
      -v /var/run/docker.sock:/var/run/docker.sock \
      starpost/jenkins-with-docker
```

This exposes the possibility of building the source with
another container.



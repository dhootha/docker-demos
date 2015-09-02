# Docker in Docker

This container illustrates how to run Docker inside of Docker.

This work is mostly stolen shamelessly from
[jpettazo](http://github.com/jpetazzo/dind). See the original work for
more information.

---

# Build

```
docker build -t dind .
```

---

# Use

Execute with a shell (logs to stdout)

```
docker run --privileged -t -i dind
```

--

Run with a shell (logs to /var/log/docker.log)

docker run --privileged -t -i -e LOG=file dind





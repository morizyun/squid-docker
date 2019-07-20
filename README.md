# squid-docker

* GitHub: https://github.com/morizyun/squid-docker
* DockerHub: https://hub.docker.com/r/morizyun/squid-docker/

## How to start

```bash
# Start with password
docker run -p 49834:3128 -dit \
    --restart unless-stopped \
    -e SQUID_USERNAME=hoge \
    -e SQUID_PASSWORD=fuga \
    morizyun/squid-docker
```

## Confirm

Run it on a server, since localhost does not recognize Proxy.

```bash
# Confirm Proxy with password
curl --proxy http://hoge:fuga@SERVER_IP:49834 https://www.ugtop.com/spill.shtml
```

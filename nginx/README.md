# nginx

Docker compose configuration for nginx web server.

## Usage

- Create an external network named `nginx_network`:

```bash
docker network create nginx-network
```

Then connect your other containers to this network in docker-compose.yml:

```yaml
networks:
  nginx-network:
    external: true

services:
    your-service:
        # image: ....
        # omitted for brevity
        networks:
            - nginx-network
```

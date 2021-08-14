# Traefik

## Run

```sh
> docker network create proxy
> docker-compose up -d
```

## Usage

Add these labels to your service in `docker-compose.yml`

```yml
  labels:
    - traefik.http.routers.sample.rule=Host(`sample.localhost`)
    - traefik.http.routers.sample.tls=true
    - traefik.http.routers.sample.tls.certresolver=lets-encrypt
    - traefik.port=80
```

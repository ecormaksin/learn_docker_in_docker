# Temporary memo

```shell
docker buildx build -t localhost/dind-client:latest -f ./client/Containerfile .
```

```shell
docker run -d -h dind-client --runtime=sysbox-runc -v ./containers:/containers localhost/dind-client:latest
```

```shell
docker compose --file ./compose-client.yaml up -d
```

```shell
docker compose --file ./compose-dind.yaml up -d
```
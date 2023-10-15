# Temporary memo

```shell
docker buildx build -t localhost/dind-client:latest -f ./client/Containerfile .
```

```shell
docker run -d -h dind-client --name=dind-client-01 --runtime=sysbox-runc -v ./containers:/containers localhost/dind-client:latest
```

```shell
docker compose --file ./compose-client.yaml up -d
```

```shell
docker compose --file ./compose-dind.yaml up -d
```

```shell
docker run -d -h dind-rootless-client-01 --name=dind-rootless-client-01 --privileged --runtime=sysbox-runc -v ./containers:/containers docker.io/library/docker:dind-rootless
```

```shell
docker inspect --format='{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' $INSTANCE_ID
```

```shell
aws s3api list-buckets --endpoint-url http://localhost:4566 --profile localstack
```
